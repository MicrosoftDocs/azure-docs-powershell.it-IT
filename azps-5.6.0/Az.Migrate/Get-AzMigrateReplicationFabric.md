---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 25106d6facb65346360bf7c78b7cbef27fc9a517
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982941"
---
# <span data-ttu-id="16953-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="16953-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="16953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16953-102">SYNOPSIS</span></span>
<span data-ttu-id="16953-103">Recupera i dettagli di un tessuto Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="16953-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="16953-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16953-104">SYNTAX</span></span>

### <span data-ttu-id="16953-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16953-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16953-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="16953-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="16953-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16953-107">DESCRIPTION</span></span>
<span data-ttu-id="16953-108">Recupera i dettagli di un tessuto Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="16953-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="16953-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16953-109">EXAMPLES</span></span>

### <span data-ttu-id="16953-110">Esempio 1: Ottenere tutte le tessuto per gruppo di risorse e nome vault</span><span class="sxs-lookup"><span data-stu-id="16953-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="16953-111">Recuperare tutte le tessuto nel gruppo di risorse e nel vault</span><span class="sxs-lookup"><span data-stu-id="16953-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="16953-112">Esempio 2: Ottenere tessuto per gruppo di risorse, nome del vault e nome del tessuto</span><span class="sxs-lookup"><span data-stu-id="16953-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="16953-113">Ottenere un tessuto specifico</span><span class="sxs-lookup"><span data-stu-id="16953-113">Get a specific fabric</span></span>

## <span data-ttu-id="16953-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16953-114">PARAMETERS</span></span>

### <span data-ttu-id="16953-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16953-115">-DefaultProfile</span></span>
<span data-ttu-id="16953-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16953-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16953-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="16953-117">-FabricName</span></span>
<span data-ttu-id="16953-118">Nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="16953-118">Fabric name.</span></span>

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

### <span data-ttu-id="16953-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16953-119">-ResourceGroupName</span></span>
<span data-ttu-id="16953-120">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="16953-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="16953-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="16953-121">-ResourceName</span></span>
<span data-ttu-id="16953-122">Nome del vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="16953-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="16953-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16953-123">-SubscriptionId</span></span>
<span data-ttu-id="16953-124">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="16953-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="16953-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16953-125">CommonParameters</span></span>
<span data-ttu-id="16953-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16953-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16953-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16953-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16953-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="16953-128">INPUTS</span></span>

## <span data-ttu-id="16953-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16953-129">OUTPUTS</span></span>

### <span data-ttu-id="16953-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="16953-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="16953-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="16953-131">NOTES</span></span>

<span data-ttu-id="16953-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="16953-132">ALIASES</span></span>

## <span data-ttu-id="16953-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16953-133">RELATED LINKS</span></span>

