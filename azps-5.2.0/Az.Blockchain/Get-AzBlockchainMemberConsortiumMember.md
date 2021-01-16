---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341911"
---
# <span data-ttu-id="311d5-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="311d5-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="311d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="311d5-102">SYNOPSIS</span></span>
<span data-ttu-id="311d5-103">Elenca i membri del Consorzio per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="311d5-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="311d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="311d5-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="311d5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="311d5-105">DESCRIPTION</span></span>
<span data-ttu-id="311d5-106">Elenca i membri del Consorzio per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="311d5-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="311d5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="311d5-107">EXAMPLES</span></span>

### <span data-ttu-id="311d5-108">Esempio 1: elenca i membri del Consorzio per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="311d5-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="311d5-109">Questo comando elenca i membri del Consorzio per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="311d5-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="311d5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="311d5-110">PARAMETERS</span></span>

### <span data-ttu-id="311d5-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="311d5-111">-BlockchainMemberName</span></span>
<span data-ttu-id="311d5-112">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="311d5-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="311d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311d5-113">-DefaultProfile</span></span>
<span data-ttu-id="311d5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="311d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="311d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="311d5-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="311d5-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="311d5-117">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="311d5-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="311d5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="311d5-118">-SubscriptionId</span></span>
<span data-ttu-id="311d5-119">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="311d5-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="311d5-120">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="311d5-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="311d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311d5-121">CommonParameters</span></span>
<span data-ttu-id="311d5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311d5-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="311d5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311d5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="311d5-124">INPUTS</span></span>

## <span data-ttu-id="311d5-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="311d5-125">OUTPUTS</span></span>

### <span data-ttu-id="311d5-126">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="311d5-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="311d5-127">Note</span><span class="sxs-lookup"><span data-stu-id="311d5-127">NOTES</span></span>

<span data-ttu-id="311d5-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="311d5-128">ALIASES</span></span>

## <span data-ttu-id="311d5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="311d5-129">RELATED LINKS</span></span>

