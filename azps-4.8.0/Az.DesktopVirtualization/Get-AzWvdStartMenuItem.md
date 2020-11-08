---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190751"
---
# <span data-ttu-id="9315b-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="9315b-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="9315b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9315b-102">SYNOPSIS</span></span>
<span data-ttu-id="9315b-103">Voci di menu Start elenco nel gruppo di applicazioni specifico.</span><span class="sxs-lookup"><span data-stu-id="9315b-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="9315b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9315b-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9315b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9315b-105">DESCRIPTION</span></span>
<span data-ttu-id="9315b-106">Voci di menu Start elenco nel gruppo di applicazioni specifico.</span><span class="sxs-lookup"><span data-stu-id="9315b-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="9315b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9315b-107">EXAMPLES</span></span>

### <span data-ttu-id="9315b-108">Esempio 2: elenco delle voci di menu Start di Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="9315b-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="9315b-109">Questo comando elenca le voci di menu Start di Windows Virtual Desktop in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="9315b-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="9315b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9315b-110">PARAMETERS</span></span>

### <span data-ttu-id="9315b-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="9315b-111">-ApplicationGroupName</span></span>
<span data-ttu-id="9315b-112">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="9315b-112">The name of the application group</span></span>

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

### <span data-ttu-id="9315b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9315b-113">-DefaultProfile</span></span>
<span data-ttu-id="9315b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9315b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9315b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9315b-115">-ResourceGroupName</span></span>
<span data-ttu-id="9315b-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9315b-116">The name of the resource group.</span></span>
<span data-ttu-id="9315b-117">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9315b-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9315b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9315b-118">-SubscriptionId</span></span>
<span data-ttu-id="9315b-119">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9315b-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9315b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9315b-120">CommonParameters</span></span>
<span data-ttu-id="9315b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9315b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9315b-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9315b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9315b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9315b-123">INPUTS</span></span>

## <span data-ttu-id="9315b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9315b-124">OUTPUTS</span></span>

### <span data-ttu-id="9315b-125">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="9315b-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="9315b-126">Note</span><span class="sxs-lookup"><span data-stu-id="9315b-126">NOTES</span></span>

<span data-ttu-id="9315b-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9315b-127">ALIASES</span></span>

## <span data-ttu-id="9315b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9315b-128">RELATED LINKS</span></span>
