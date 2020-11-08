---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "94023043"
---
# <span data-ttu-id="86444-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="86444-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="86444-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86444-102">SYNOPSIS</span></span>


## <span data-ttu-id="86444-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86444-103">SYNTAX</span></span>

### <span data-ttu-id="86444-104">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86444-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="86444-105">Ottieni</span><span class="sxs-lookup"><span data-stu-id="86444-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="86444-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="86444-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="86444-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86444-107">DESCRIPTION</span></span>


## <span data-ttu-id="86444-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86444-108">EXAMPLES</span></span>

### <span data-ttu-id="86444-109">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="86444-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="86444-110">Ottenere l'elenco delle quote di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="86444-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="86444-111">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="86444-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="86444-112">Ottenere i dettagli della quota di archiviazione specificata per nome.</span><span class="sxs-lookup"><span data-stu-id="86444-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="86444-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86444-113">PARAMETERS</span></span>

### <span data-ttu-id="86444-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86444-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="86444-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86444-115">-InputObject</span></span>
<span data-ttu-id="86444-116">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="86444-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="86444-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="86444-117">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="86444-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="86444-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="86444-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86444-119">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="86444-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86444-120">CommonParameters</span></span>
<span data-ttu-id="86444-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86444-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86444-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86444-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86444-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86444-123">INPUTS</span></span>

### <span data-ttu-id="86444-124">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="86444-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="86444-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86444-125">OUTPUTS</span></span>

### <span data-ttu-id="86444-126">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="86444-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="86444-127">Note</span><span class="sxs-lookup"><span data-stu-id="86444-127">NOTES</span></span>

<span data-ttu-id="86444-128">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="86444-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86444-129">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86444-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="86444-130">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="86444-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="86444-131">`[AccountId <String>]`: ID account di archiviazione interno, che non è visibile al tenant.</span><span class="sxs-lookup"><span data-stu-id="86444-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="86444-132">`[AsyncOperationId <String>]`: ID operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="86444-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="86444-133">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="86444-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86444-134">`[Location <String>]`: Percorso delle risorse.</span><span class="sxs-lookup"><span data-stu-id="86444-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="86444-135">`[QuotaName <String>]`: Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="86444-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="86444-136">`[ResourceGroup <String>]`: Nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="86444-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="86444-137">`[ServiceName <String>]`: Nome servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="86444-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="86444-138">`[SubscriptionId <String>]`: ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="86444-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="86444-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86444-139">RELATED LINKS</span></span>

