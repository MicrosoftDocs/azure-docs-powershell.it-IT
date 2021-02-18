---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200927"
---
# <span data-ttu-id="130ce-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="130ce-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="130ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="130ce-102">SYNOPSIS</span></span>
<span data-ttu-id="130ce-103">Elenca i membri del consorzio per un membro member member di member member.</span><span class="sxs-lookup"><span data-stu-id="130ce-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="130ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="130ce-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="130ce-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="130ce-105">DESCRIPTION</span></span>
<span data-ttu-id="130ce-106">Elenca i membri del consorzio per un membro member member di member member.</span><span class="sxs-lookup"><span data-stu-id="130ce-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="130ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="130ce-107">EXAMPLES</span></span>

### <span data-ttu-id="130ce-108">Esempio 1: elenca i membri del consorzio per un membro modello.</span><span class="sxs-lookup"><span data-stu-id="130ce-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="130ce-109">Questo comando elenca i membri del consorzio per un membro member member member.</span><span class="sxs-lookup"><span data-stu-id="130ce-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="130ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="130ce-110">PARAMETERS</span></span>

### <span data-ttu-id="130ce-111">-MemberName</span><span class="sxs-lookup"><span data-stu-id="130ce-111">-BlockchainMemberName</span></span>
<span data-ttu-id="130ce-112">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="130ce-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="130ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="130ce-113">-DefaultProfile</span></span>
<span data-ttu-id="130ce-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="130ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="130ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="130ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="130ce-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="130ce-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="130ce-117">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="130ce-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="130ce-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="130ce-118">-SubscriptionId</span></span>
<span data-ttu-id="130ce-119">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="130ce-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="130ce-120">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="130ce-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="130ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="130ce-121">CommonParameters</span></span>
<span data-ttu-id="130ce-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="130ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="130ce-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="130ce-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="130ce-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="130ce-124">INPUTS</span></span>

## <span data-ttu-id="130ce-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="130ce-125">OUTPUTS</span></span>

### <span data-ttu-id="130ce-126">Microsoft.Azure.PowerShell.Cmdlets.Kpi.Models.Api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="130ce-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="130ce-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="130ce-127">NOTES</span></span>

<span data-ttu-id="130ce-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="130ce-128">ALIASES</span></span>

## <span data-ttu-id="130ce-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="130ce-129">RELATED LINKS</span></span>

