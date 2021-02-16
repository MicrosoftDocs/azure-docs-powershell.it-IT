---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: e2cad9282e1e662cee58625a17c3f0672947d26a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190174"
---
# <span data-ttu-id="d77d6-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d77d6-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="d77d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d77d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d77d6-103">Recupera i dettagli di un criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="d77d6-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="d77d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d77d6-104">SYNTAX</span></span>

### <span data-ttu-id="d77d6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d77d6-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d77d6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d77d6-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d77d6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d77d6-107">DESCRIPTION</span></span>
<span data-ttu-id="d77d6-108">Recupera i dettagli di un criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="d77d6-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="d77d6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d77d6-109">EXAMPLES</span></span>

### <span data-ttu-id="d77d6-110">Esempio 1: Ottenere tutti i criteri in un vault</span><span class="sxs-lookup"><span data-stu-id="d77d6-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="d77d6-111">Ottenere tutti i criteri.</span><span class="sxs-lookup"><span data-stu-id="d77d6-111">Get all policies.</span></span>

### <span data-ttu-id="d77d6-112">Esempio 2: Ottenere un criterio specifico</span><span class="sxs-lookup"><span data-stu-id="d77d6-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="d77d6-113">Ottieni un modello specifico.</span><span class="sxs-lookup"><span data-stu-id="d77d6-113">Get a specific one.</span></span>

## <span data-ttu-id="d77d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d77d6-114">PARAMETERS</span></span>

### <span data-ttu-id="d77d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77d6-115">-DefaultProfile</span></span>
<span data-ttu-id="d77d6-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d77d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d77d6-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="d77d6-117">-PolicyName</span></span>
<span data-ttu-id="d77d6-118">Nome del criterio di replica.</span><span class="sxs-lookup"><span data-stu-id="d77d6-118">Replication policy name.</span></span>

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

### <span data-ttu-id="d77d6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d77d6-119">-ResourceGroupName</span></span>
<span data-ttu-id="d77d6-120">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d77d6-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="d77d6-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d77d6-121">-ResourceName</span></span>
<span data-ttu-id="d77d6-122">Nome del vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d77d6-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="d77d6-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d77d6-123">-SubscriptionId</span></span>
<span data-ttu-id="d77d6-124">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="d77d6-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d77d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77d6-125">CommonParameters</span></span>
<span data-ttu-id="d77d6-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d77d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77d6-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d77d6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77d6-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="d77d6-128">INPUTS</span></span>

## <span data-ttu-id="d77d6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d77d6-129">OUTPUTS</span></span>

### <span data-ttu-id="d77d6-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="d77d6-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="d77d6-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="d77d6-131">NOTES</span></span>

<span data-ttu-id="d77d6-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d77d6-132">ALIASES</span></span>

## <span data-ttu-id="d77d6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d77d6-133">RELATED LINKS</span></span>

