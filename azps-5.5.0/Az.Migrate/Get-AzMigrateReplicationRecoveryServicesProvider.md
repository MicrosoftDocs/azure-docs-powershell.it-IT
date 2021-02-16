---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: e706e9eb21f601ed1a266faa0afb888297f17fdb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190158"
---
# <span data-ttu-id="3de1d-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3de1d-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="3de1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3de1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3de1d-103">Recupera i dettagli del provider di servizi di ripristino registrati.</span><span class="sxs-lookup"><span data-stu-id="3de1d-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="3de1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3de1d-104">SYNTAX</span></span>

### <span data-ttu-id="3de1d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3de1d-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3de1d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3de1d-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3de1d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3de1d-107">DESCRIPTION</span></span>
<span data-ttu-id="3de1d-108">Recupera i dettagli del provider di servizi di ripristino registrati.</span><span class="sxs-lookup"><span data-stu-id="3de1d-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="3de1d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3de1d-109">EXAMPLES</span></span>

### <span data-ttu-id="3de1d-110">Esempio 1: Ottenere tutti i provider nel Vault</span><span class="sxs-lookup"><span data-stu-id="3de1d-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="3de1d-111">Elencare tutto.</span><span class="sxs-lookup"><span data-stu-id="3de1d-111">List all.</span></span>

## <span data-ttu-id="3de1d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3de1d-112">PARAMETERS</span></span>

### <span data-ttu-id="3de1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de1d-113">-DefaultProfile</span></span>
<span data-ttu-id="3de1d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3de1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3de1d-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="3de1d-115">-FabricName</span></span>
<span data-ttu-id="3de1d-116">Nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="3de1d-116">Fabric name.</span></span>

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

### <span data-ttu-id="3de1d-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="3de1d-117">-ProviderName</span></span>
<span data-ttu-id="3de1d-118">Nome del provider di servizi di ripristino</span><span class="sxs-lookup"><span data-stu-id="3de1d-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="3de1d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de1d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3de1d-120">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3de1d-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="3de1d-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3de1d-121">-ResourceName</span></span>
<span data-ttu-id="3de1d-122">Nome del vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3de1d-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="3de1d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3de1d-123">-SubscriptionId</span></span>
<span data-ttu-id="3de1d-124">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="3de1d-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="3de1d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de1d-125">CommonParameters</span></span>
<span data-ttu-id="3de1d-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de1d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de1d-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3de1d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de1d-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="3de1d-128">INPUTS</span></span>

## <span data-ttu-id="3de1d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3de1d-129">OUTPUTS</span></span>

### <span data-ttu-id="3de1d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3de1d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="3de1d-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="3de1d-131">NOTES</span></span>

<span data-ttu-id="3de1d-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3de1d-132">ALIASES</span></span>

## <span data-ttu-id="3de1d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3de1d-133">RELATED LINKS</span></span>

