---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: a2db8d344628d8a421623cd5e6348db31a7321ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980558"
---
# <span data-ttu-id="1f595-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="1f595-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="1f595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f595-102">SYNOPSIS</span></span>
<span data-ttu-id="1f595-103">Elencare le voci del menu Start nel gruppo di applicazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="1f595-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="1f595-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f595-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1f595-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f595-105">DESCRIPTION</span></span>
<span data-ttu-id="1f595-106">Elencare le voci del menu Start nel gruppo di applicazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="1f595-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="1f595-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f595-107">EXAMPLES</span></span>

### <span data-ttu-id="1f595-108">Esempio 2: Elencare le voci del menu Start del desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="1f595-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="1f595-109">Questo comando elenca le voci del menu Start del desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="1f595-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="1f595-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f595-110">PARAMETERS</span></span>

### <span data-ttu-id="1f595-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="1f595-111">-ApplicationGroupName</span></span>
<span data-ttu-id="1f595-112">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="1f595-112">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f595-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f595-113">-DefaultProfile</span></span>
<span data-ttu-id="1f595-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f595-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f595-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f595-115">-ResourceGroupName</span></span>
<span data-ttu-id="1f595-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f595-116">The name of the resource group.</span></span>
<span data-ttu-id="1f595-117">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1f595-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f595-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f595-118">-SubscriptionId</span></span>
<span data-ttu-id="1f595-119">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f595-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f595-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f595-120">CommonParameters</span></span>
<span data-ttu-id="1f595-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f595-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f595-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f595-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f595-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f595-123">INPUTS</span></span>

## <span data-ttu-id="1f595-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f595-124">OUTPUTS</span></span>

### <span data-ttu-id="1f595-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="1f595-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="1f595-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f595-126">NOTES</span></span>

<span data-ttu-id="1f595-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1f595-127">ALIASES</span></span>

## <span data-ttu-id="1f595-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f595-128">RELATED LINKS</span></span>

