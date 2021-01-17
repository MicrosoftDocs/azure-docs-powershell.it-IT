---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342835"
---
# <span data-ttu-id="6eee9-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="6eee9-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="6eee9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6eee9-102">SYNOPSIS</span></span>
<span data-ttu-id="6eee9-103">Ottiene i dettagli di un criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="6eee9-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="6eee9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6eee9-104">SYNTAX</span></span>

### <span data-ttu-id="6eee9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6eee9-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6eee9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="6eee9-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6eee9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6eee9-107">DESCRIPTION</span></span>
<span data-ttu-id="6eee9-108">Ottiene i dettagli di un criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="6eee9-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="6eee9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6eee9-109">EXAMPLES</span></span>

### <span data-ttu-id="6eee9-110">Esempio 1: ottenere tutti i criteri in un Vault</span><span class="sxs-lookup"><span data-stu-id="6eee9-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="6eee9-111">Ottenere tutti i criteri.</span><span class="sxs-lookup"><span data-stu-id="6eee9-111">Get all policies.</span></span>

### <span data-ttu-id="6eee9-112">Esempio 2: ottenere un criterio specifico</span><span class="sxs-lookup"><span data-stu-id="6eee9-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="6eee9-113">Ottenere uno specifico.</span><span class="sxs-lookup"><span data-stu-id="6eee9-113">Get a specific one.</span></span>

## <span data-ttu-id="6eee9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6eee9-114">PARAMETERS</span></span>

### <span data-ttu-id="6eee9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eee9-115">-DefaultProfile</span></span>
<span data-ttu-id="6eee9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6eee9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eee9-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="6eee9-117">-PolicyName</span></span>
<span data-ttu-id="6eee9-118">Nome criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="6eee9-118">Replication policy name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eee9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eee9-119">-ResourceGroupName</span></span>
<span data-ttu-id="6eee9-120">Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6eee9-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="6eee9-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6eee9-121">-ResourceName</span></span>
<span data-ttu-id="6eee9-122">Nome del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6eee9-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="6eee9-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6eee9-123">-SubscriptionId</span></span>
<span data-ttu-id="6eee9-124">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6eee9-124">The subscription Id.</span></span>

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

### <span data-ttu-id="6eee9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eee9-125">CommonParameters</span></span>
<span data-ttu-id="6eee9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eee9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eee9-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6eee9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eee9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6eee9-128">INPUTS</span></span>

## <span data-ttu-id="6eee9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6eee9-129">OUTPUTS</span></span>

### <span data-ttu-id="6eee9-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="6eee9-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="6eee9-131">Note</span><span class="sxs-lookup"><span data-stu-id="6eee9-131">NOTES</span></span>

<span data-ttu-id="6eee9-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6eee9-132">ALIASES</span></span>

## <span data-ttu-id="6eee9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6eee9-133">RELATED LINKS</span></span>

