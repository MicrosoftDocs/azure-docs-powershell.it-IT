---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330832"
---
# <span data-ttu-id="b9275-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="b9275-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="b9275-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9275-102">SYNOPSIS</span></span>
<span data-ttu-id="b9275-103">Ottiene i dettagli di un tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="b9275-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="b9275-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9275-104">SYNTAX</span></span>

### <span data-ttu-id="b9275-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9275-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9275-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b9275-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b9275-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9275-107">DESCRIPTION</span></span>
<span data-ttu-id="b9275-108">Ottiene i dettagli di un tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="b9275-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="b9275-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9275-109">EXAMPLES</span></span>

### <span data-ttu-id="b9275-110">Esempio 1: ottenere tutti i tessuti per gruppo risorse e nome volta</span><span class="sxs-lookup"><span data-stu-id="b9275-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="b9275-111">Ottenere tutti i tessuti in un gruppo di risorse e un Vault</span><span class="sxs-lookup"><span data-stu-id="b9275-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="b9275-112">Esempio 2: ottenere il tessuto per gruppo di risorse, nome del Vault e nome del tessuto</span><span class="sxs-lookup"><span data-stu-id="b9275-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="b9275-113">Ottenere un tessuto specifico</span><span class="sxs-lookup"><span data-stu-id="b9275-113">Get a specific fabric</span></span>

## <span data-ttu-id="b9275-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9275-114">PARAMETERS</span></span>

### <span data-ttu-id="b9275-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9275-115">-DefaultProfile</span></span>
<span data-ttu-id="b9275-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9275-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9275-117">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="b9275-117">-FabricName</span></span>
<span data-ttu-id="b9275-118">Nome tessuto.</span><span class="sxs-lookup"><span data-stu-id="b9275-118">Fabric name.</span></span>

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

### <span data-ttu-id="b9275-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9275-119">-ResourceGroupName</span></span>
<span data-ttu-id="b9275-120">Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9275-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="b9275-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b9275-121">-ResourceName</span></span>
<span data-ttu-id="b9275-122">Nome del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9275-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="b9275-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9275-123">-SubscriptionId</span></span>
<span data-ttu-id="b9275-124">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b9275-124">The subscription Id.</span></span>

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

### <span data-ttu-id="b9275-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9275-125">CommonParameters</span></span>
<span data-ttu-id="b9275-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9275-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9275-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9275-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9275-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9275-128">INPUTS</span></span>

## <span data-ttu-id="b9275-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9275-129">OUTPUTS</span></span>

### <span data-ttu-id="b9275-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IFabric</span><span class="sxs-lookup"><span data-stu-id="b9275-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="b9275-131">Note</span><span class="sxs-lookup"><span data-stu-id="b9275-131">NOTES</span></span>

<span data-ttu-id="b9275-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b9275-132">ALIASES</span></span>

## <span data-ttu-id="b9275-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9275-133">RELATED LINKS</span></span>

