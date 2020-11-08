---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023126"
---
# <span data-ttu-id="6a29c-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="6a29c-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="6a29c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a29c-102">SYNOPSIS</span></span>


## <span data-ttu-id="6a29c-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a29c-103">SYNTAX</span></span>

### <span data-ttu-id="6a29c-104">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a29c-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a29c-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6a29c-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a29c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a29c-106">DESCRIPTION</span></span>


## <span data-ttu-id="6a29c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a29c-107">EXAMPLES</span></span>

### <span data-ttu-id="6a29c-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="6a29c-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="6a29c-109">Rimuovere una quota di archiviazione per nome.</span><span class="sxs-lookup"><span data-stu-id="6a29c-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="6a29c-110">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="6a29c-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="6a29c-111">Rimuovere una quota di archiviazione tramite piping.</span><span class="sxs-lookup"><span data-stu-id="6a29c-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="6a29c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a29c-112">PARAMETERS</span></span>

### <span data-ttu-id="6a29c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a29c-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="6a29c-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a29c-114">-InputObject</span></span>
<span data-ttu-id="6a29c-115">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6a29c-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6a29c-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6a29c-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a29c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a29c-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a29c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a29c-118">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a29c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a29c-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a29c-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a29c-120">-Confirm</span></span>
<span data-ttu-id="6a29c-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a29c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a29c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a29c-122">-WhatIf</span></span>
<span data-ttu-id="6a29c-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a29c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a29c-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a29c-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a29c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a29c-125">CommonParameters</span></span>
<span data-ttu-id="6a29c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a29c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a29c-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a29c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a29c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a29c-128">INPUTS</span></span>

### <span data-ttu-id="6a29c-129">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6a29c-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="6a29c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a29c-130">OUTPUTS</span></span>

### <span data-ttu-id="6a29c-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a29c-131">System.Boolean</span></span>



## <span data-ttu-id="6a29c-132">Note</span><span class="sxs-lookup"><span data-stu-id="6a29c-132">NOTES</span></span>

<span data-ttu-id="6a29c-133">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6a29c-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a29c-134">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a29c-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6a29c-135">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="6a29c-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="6a29c-136">`[AccountId <String>]`: ID account di archiviazione interno, che non è visibile al tenant.</span><span class="sxs-lookup"><span data-stu-id="6a29c-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="6a29c-137">`[AsyncOperationId <String>]`: ID operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="6a29c-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="6a29c-138">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6a29c-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a29c-139">`[Location <String>]`: Percorso delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6a29c-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="6a29c-140">`[QuotaName <String>]`: Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a29c-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="6a29c-141">`[ResourceGroup <String>]`: Nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="6a29c-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="6a29c-142">`[ServiceName <String>]`: Nome servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a29c-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="6a29c-143">`[SubscriptionId <String>]`: ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6a29c-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="6a29c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a29c-144">RELATED LINKS</span></span>

