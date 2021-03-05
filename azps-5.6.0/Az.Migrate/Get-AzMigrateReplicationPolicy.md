---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 261d7467d67708380f86c8df061fdda02eb095c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982925"
---
# <span data-ttu-id="33834-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="33834-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="33834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33834-102">SYNOPSIS</span></span>
<span data-ttu-id="33834-103">Recupera i dettagli di un criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="33834-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="33834-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33834-104">SYNTAX</span></span>

### <span data-ttu-id="33834-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33834-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="33834-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="33834-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="33834-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33834-107">DESCRIPTION</span></span>
<span data-ttu-id="33834-108">Recupera i dettagli di un criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="33834-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="33834-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33834-109">EXAMPLES</span></span>

### <span data-ttu-id="33834-110">Esempio 1: Ottenere tutti i criteri in un vault</span><span class="sxs-lookup"><span data-stu-id="33834-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="33834-111">Ottenere tutti i criteri.</span><span class="sxs-lookup"><span data-stu-id="33834-111">Get all policies.</span></span>

### <span data-ttu-id="33834-112">Esempio 2: Ottenere un criterio specifico</span><span class="sxs-lookup"><span data-stu-id="33834-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="33834-113">Ottieni un modello specifico.</span><span class="sxs-lookup"><span data-stu-id="33834-113">Get a specific one.</span></span>

## <span data-ttu-id="33834-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33834-114">PARAMETERS</span></span>

### <span data-ttu-id="33834-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33834-115">-DefaultProfile</span></span>
<span data-ttu-id="33834-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33834-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33834-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="33834-117">-PolicyName</span></span>
<span data-ttu-id="33834-118">Nome del criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="33834-118">Replication policy name.</span></span>

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

### <span data-ttu-id="33834-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33834-119">-ResourceGroupName</span></span>
<span data-ttu-id="33834-120">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="33834-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="33834-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="33834-121">-ResourceName</span></span>
<span data-ttu-id="33834-122">Nome del vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="33834-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="33834-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33834-123">-SubscriptionId</span></span>
<span data-ttu-id="33834-124">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="33834-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="33834-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33834-125">CommonParameters</span></span>
<span data-ttu-id="33834-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33834-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33834-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33834-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33834-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="33834-128">INPUTS</span></span>

## <span data-ttu-id="33834-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33834-129">OUTPUTS</span></span>

### <span data-ttu-id="33834-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="33834-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="33834-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="33834-131">NOTES</span></span>

<span data-ttu-id="33834-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="33834-132">ALIASES</span></span>

## <span data-ttu-id="33834-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33834-133">RELATED LINKS</span></span>

