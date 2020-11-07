---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861665"
---
# <span data-ttu-id="a4914-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a4914-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="a4914-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4914-102">SYNOPSIS</span></span>
<span data-ttu-id="a4914-103">Restituisce l'account di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="a4914-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="a4914-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4914-104">SYNTAX</span></span>

### <span data-ttu-id="a4914-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4914-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4914-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a4914-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4914-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4914-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a4914-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4914-108">DESCRIPTION</span></span>
<span data-ttu-id="a4914-109">Restituisce l'account di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="a4914-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="a4914-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4914-110">EXAMPLES</span></span>

### <span data-ttu-id="a4914-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="a4914-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="a4914-112">Ottenere un elenco di account di archiviazione (riepilogo).</span><span class="sxs-lookup"><span data-stu-id="a4914-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="a4914-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="a4914-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="a4914-114">Ottenere un elenco di account di archiviazione con i dettagli e stampare lo stato.</span><span class="sxs-lookup"><span data-stu-id="a4914-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="a4914-115">Esempio 3:</span><span class="sxs-lookup"><span data-stu-id="a4914-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="a4914-116">Ottenere i dettagli dell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a4914-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="a4914-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4914-117">PARAMETERS</span></span>

### <span data-ttu-id="a4914-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4914-118">-DefaultProfile</span></span>
<span data-ttu-id="a4914-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4914-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4914-120">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a4914-120">-Filter</span></span>
<span data-ttu-id="a4914-121">Stringa di filtro</span><span class="sxs-lookup"><span data-stu-id="a4914-121">Filter string</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4914-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4914-122">-InputObject</span></span>
<span data-ttu-id="a4914-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a4914-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a4914-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a4914-124">-Location</span></span>
<span data-ttu-id="a4914-125">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a4914-125">Resource location.</span></span>

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

### <span data-ttu-id="a4914-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4914-126">-Name</span></span>
<span data-ttu-id="a4914-127">ID account di archiviazione interno, che non è visibile al tenant.</span><span class="sxs-lookup"><span data-stu-id="a4914-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4914-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4914-128">-SubscriptionId</span></span>
<span data-ttu-id="a4914-129">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a4914-129">Subscription Id.</span></span>

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

### <span data-ttu-id="a4914-130">-Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a4914-130">-Summary</span></span>
<span data-ttu-id="a4914-131">Opzione per specificare se vengono restituiti informazioni di riepilogo o dettagliate.</span><span class="sxs-lookup"><span data-stu-id="a4914-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4914-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4914-132">CommonParameters</span></span>
<span data-ttu-id="a4914-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4914-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4914-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4914-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4914-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4914-135">INPUTS</span></span>

### <span data-ttu-id="a4914-136">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a4914-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="a4914-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4914-137">OUTPUTS</span></span>

### <span data-ttu-id="a4914-138">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a4914-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="a4914-139">Note</span><span class="sxs-lookup"><span data-stu-id="a4914-139">NOTES</span></span>

<span data-ttu-id="a4914-140">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a4914-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4914-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4914-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a4914-142">INPUTOBJECT <IStorageAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a4914-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4914-143">`[AccountId <String>]`: ID account di archiviazione interno, che non è visibile al tenant.</span><span class="sxs-lookup"><span data-stu-id="a4914-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="a4914-144">`[AsyncOperationId <String>]`: ID operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a4914-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="a4914-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a4914-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4914-146">`[Location <String>]`: Percorso delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a4914-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="a4914-147">`[QuotaName <String>]`: Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a4914-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="a4914-148">`[ResourceGroup <String>]`: Nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="a4914-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="a4914-149">`[ServiceName <String>]`: Nome servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a4914-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="a4914-150">`[SubscriptionId <String>]`: ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a4914-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="a4914-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4914-151">RELATED LINKS</span></span>

