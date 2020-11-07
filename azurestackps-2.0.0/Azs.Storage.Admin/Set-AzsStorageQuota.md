---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861654"
---
# <span data-ttu-id="569b4-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="569b4-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="569b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="569b4-102">SYNOPSIS</span></span>


## <span data-ttu-id="569b4-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="569b4-103">SYNTAX</span></span>

### <span data-ttu-id="569b4-104">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="569b4-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="569b4-105">QuotaObject</span><span class="sxs-lookup"><span data-stu-id="569b4-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="569b4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="569b4-106">DESCRIPTION</span></span>


## <span data-ttu-id="569b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="569b4-107">EXAMPLES</span></span>

### <span data-ttu-id="569b4-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="569b4-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="569b4-109">Aggiornare una quota di archiviazione esistente per nome.</span><span class="sxs-lookup"><span data-stu-id="569b4-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="569b4-110">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="569b4-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="569b4-111">Aggiornare una quota di archiviazione esistente tramite piping.</span><span class="sxs-lookup"><span data-stu-id="569b4-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="569b4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="569b4-112">PARAMETERS</span></span>

### <span data-ttu-id="569b4-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="569b4-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="569b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569b4-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="569b4-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="569b4-115">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="569b4-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="569b4-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="569b4-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="569b4-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="569b4-118">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="569b4-118">-QuotaObject</span></span>
<span data-ttu-id="569b4-119">Per costruire, vedere la sezione Note per le proprietà di QUOTAOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="569b4-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="569b4-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="569b4-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="569b4-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="569b4-121">-Confirm</span></span>
<span data-ttu-id="569b4-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="569b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="569b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="569b4-123">-WhatIf</span></span>
<span data-ttu-id="569b4-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="569b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="569b4-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="569b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="569b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569b4-126">CommonParameters</span></span>
<span data-ttu-id="569b4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="569b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569b4-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="569b4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569b4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="569b4-129">INPUTS</span></span>

### <span data-ttu-id="569b4-130">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="569b4-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="569b4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="569b4-131">OUTPUTS</span></span>

### <span data-ttu-id="569b4-132">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="569b4-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="569b4-133">Note</span><span class="sxs-lookup"><span data-stu-id="569b4-133">NOTES</span></span>

<span data-ttu-id="569b4-134">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="569b4-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="569b4-135">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="569b4-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="569b4-136">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="569b4-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="569b4-137">`[CapacityInGb <Int32?>]`: Capacità massima (GB).</span><span class="sxs-lookup"><span data-stu-id="569b4-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="569b4-138">`[NumberOfStorageAccounts <Int32?>]`: Numero totale di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="569b4-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="569b4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="569b4-139">RELATED LINKS</span></span>

