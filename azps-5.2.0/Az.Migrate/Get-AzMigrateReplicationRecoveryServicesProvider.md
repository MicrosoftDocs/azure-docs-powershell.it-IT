---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369946"
---
# <span data-ttu-id="ef474-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ef474-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="ef474-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef474-102">SYNOPSIS</span></span>
<span data-ttu-id="ef474-103">Ottiene i dettagli del provider di servizi di ripristino registrato.</span><span class="sxs-lookup"><span data-stu-id="ef474-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="ef474-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef474-104">SYNTAX</span></span>

### <span data-ttu-id="ef474-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef474-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef474-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ef474-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef474-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef474-107">DESCRIPTION</span></span>
<span data-ttu-id="ef474-108">Ottiene i dettagli del provider di servizi di ripristino registrato.</span><span class="sxs-lookup"><span data-stu-id="ef474-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="ef474-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef474-109">EXAMPLES</span></span>

### <span data-ttu-id="ef474-110">Esempio 1: ottenere tutti i provider in Vault</span><span class="sxs-lookup"><span data-stu-id="ef474-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="ef474-111">Elenca tutti.</span><span class="sxs-lookup"><span data-stu-id="ef474-111">List all.</span></span>

## <span data-ttu-id="ef474-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef474-112">PARAMETERS</span></span>

### <span data-ttu-id="ef474-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef474-113">-DefaultProfile</span></span>
<span data-ttu-id="ef474-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef474-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef474-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="ef474-115">-FabricName</span></span>
<span data-ttu-id="ef474-116">Nome tessuto.</span><span class="sxs-lookup"><span data-stu-id="ef474-116">Fabric name.</span></span>

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

### <span data-ttu-id="ef474-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="ef474-117">-ProviderName</span></span>
<span data-ttu-id="ef474-118">Nome provider servizi di ripristino</span><span class="sxs-lookup"><span data-stu-id="ef474-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="ef474-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef474-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef474-120">Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ef474-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="ef474-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ef474-121">-ResourceName</span></span>
<span data-ttu-id="ef474-122">Nome del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ef474-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="ef474-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef474-123">-SubscriptionId</span></span>
<span data-ttu-id="ef474-124">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ef474-124">The subscription Id.</span></span>

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

### <span data-ttu-id="ef474-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef474-125">CommonParameters</span></span>
<span data-ttu-id="ef474-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef474-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef474-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef474-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef474-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef474-128">INPUTS</span></span>

## <span data-ttu-id="ef474-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef474-129">OUTPUTS</span></span>

### <span data-ttu-id="ef474-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ef474-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="ef474-131">Note</span><span class="sxs-lookup"><span data-stu-id="ef474-131">NOTES</span></span>

<span data-ttu-id="ef474-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ef474-132">ALIASES</span></span>

## <span data-ttu-id="ef474-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef474-133">RELATED LINKS</span></span>

