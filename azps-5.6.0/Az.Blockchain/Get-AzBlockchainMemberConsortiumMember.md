---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: 19901a3834716e1f2b04102c4904c059fab29397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971502"
---
# <span data-ttu-id="3453c-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="3453c-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="3453c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3453c-102">SYNOPSIS</span></span>
<span data-ttu-id="3453c-103">Elenca i membri del consorzio per un membro member member di member member.</span><span class="sxs-lookup"><span data-stu-id="3453c-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="3453c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3453c-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3453c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3453c-105">DESCRIPTION</span></span>
<span data-ttu-id="3453c-106">Elenca i membri del consorzio per un membro member member di member member.</span><span class="sxs-lookup"><span data-stu-id="3453c-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="3453c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3453c-107">EXAMPLES</span></span>

### <span data-ttu-id="3453c-108">Esempio 1: elenca i membri del consorzio per un membro modello.</span><span class="sxs-lookup"><span data-stu-id="3453c-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="3453c-109">Questo comando elenca i membri del consorzio per un membro member member member di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="3453c-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="3453c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3453c-110">PARAMETERS</span></span>

### <span data-ttu-id="3453c-111">-MemberName</span><span class="sxs-lookup"><span data-stu-id="3453c-111">-BlockchainMemberName</span></span>
<span data-ttu-id="3453c-112">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="3453c-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="3453c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3453c-113">-DefaultProfile</span></span>
<span data-ttu-id="3453c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3453c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3453c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3453c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3453c-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3453c-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3453c-117">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="3453c-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3453c-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3453c-118">-SubscriptionId</span></span>
<span data-ttu-id="3453c-119">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3453c-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3453c-120">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3453c-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3453c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3453c-121">CommonParameters</span></span>
<span data-ttu-id="3453c-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3453c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3453c-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3453c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3453c-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="3453c-124">INPUTS</span></span>

## <span data-ttu-id="3453c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3453c-125">OUTPUTS</span></span>

### <span data-ttu-id="3453c-126">Microsoft.Azure.PowerShell.Cmdlets.Kpi.Models.Api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="3453c-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="3453c-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="3453c-127">NOTES</span></span>

<span data-ttu-id="3453c-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3453c-128">ALIASES</span></span>

## <span data-ttu-id="3453c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3453c-129">RELATED LINKS</span></span>

