/**
*Test Clan Badge
*
* @author	GameFreakBoy
* @version	0.1.0
* @date		2013-10-08
* @license	CC
*/
BBLog.handle('add.plugin', {
	/** @type 	{String} 		The extension's id. 		*/
	id: 'clan-badge',
	/** @type 	{String}		The extension's name.  		*/
	name: 'Clan Badge',
	/** @type 	{String} 		The version string.		*/
	version: '0.1.0',
            case "bblog.mark.team":
                if(!BBLog.storage("init.data")) return this.callback();
                var d = BBLog.storage("init.data");
                if(window.location.href.match(/\/user\//)){
                    var username = $.trim(window.location.href.match(/\/user\/(.*?)\//)[1]);
                    var found = BBLog.searchInObject(d["team"], null, username);
                    var e = $("#profile-information");
                    if(!BBLog.elementCheck(e, action) && e.size()){
                        if(found !== null){
                            e.find("ul:first").append($('<li class="bblog-badge"><span class="bblog-badge"></span></li>').attr("data-tooltip", BBLog.t("official.bblog.member")));
                        }
                    }
                    var e = $("#user span.real-name");
                    if(e.size() && !BBLog.elementCheck(e, action)){
                        if(found !== null){
                            e.prepend($('<span class="bblog-badge"></span>').attr("data-tooltip", BBLog.t("official.bblog.member")));
                        }
                    }else if(!e.size()){
                        var e = $("#user .information");
                        if(e.size() && !BBLog.elementCheck(e, action)){
                            if(found !== null){
                                e.prepend($('<span class="bblog-badge"></span>').attr("data-tooltip", BBLog.t("official.bblog.member")));
                            }
                        }
                    }
                }
                if(window.location.href.match(/forum\/threadview/)){
                    $(".forum-threadview-post-poster").each(function(){
                        if(BBLog.elementCheck($(this), action)) return true;
                        var username = $.trim($(this).find(".forum-threadview-post-poster-name").text());
                        if(BBLog.searchInObject(d["team"], null, username)){
                            $(this).find("ul.forum-threadview-post-tags").append($('<li class="bblog-badge"><span class="bblog-badge"></span></li>').attr("data-tooltip", BBLog.t("official.bblog.member")));
                        }
                    });
                }
