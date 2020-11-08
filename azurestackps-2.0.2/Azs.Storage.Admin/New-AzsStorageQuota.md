---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030059"
---
# <span data-ttu-id="26f69-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="26f69-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="26f69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26f69-102">SYNOPSIS</span></span>


## <span data-ttu-id="26f69-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26f69-103">SYNTAX</span></span>

### <span data-ttu-id="26f69-104">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26f69-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26f69-105">Creare</span><span class="sxs-lookup"><span data-stu-id="26f69-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26f69-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26f69-106">DESCRIPTION</span></span>


## <span data-ttu-id="26f69-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26f69-107">EXAMPLES</span></span>

### <span data-ttu-id="26f69-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="26f69-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="26f69-109">Creare una nuova quota di archiviazione con valori specificati.</span><span class="sxs-lookup"><span data-stu-id="26f69-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="26f69-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26f69-110">PARAMETERS</span></span>

### <span data-ttu-id="26f69-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="26f69-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26f69-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f69-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="26f69-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="26f69-113">-Location</span></span>


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

### <span data-ttu-id="26f69-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="26f69-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26f69-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="26f69-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26f69-116">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="26f69-116">-QuotaObject</span></span>
<span data-ttu-id="26f69-117">Per costruire, vedere la sezione Note per le proprietà di QUOTAOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="26f69-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="26f69-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26f69-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="26f69-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26f69-119">-Confirm</span></span>
<span data-ttu-id="26f69-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26f69-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f69-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f69-121">-WhatIf</span></span>
<span data-ttu-id="26f69-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26f69-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f69-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26f69-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f69-124">CommonParameters</span></span>
<span data-ttu-id="26f69-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f69-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26f69-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f69-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26f69-127">INPUTS</span></span>

### <span data-ttu-id="26f69-128">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="26f69-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="26f69-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26f69-129">OUTPUTS</span></span>

### <span data-ttu-id="26f69-130">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="26f69-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="26f69-131">Note</span><span class="sxs-lookup"><span data-stu-id="26f69-131">NOTES</span></span>

<span data-ttu-id="26f69-132">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="26f69-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26f69-133">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26f69-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="26f69-134">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="26f69-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="26f69-135">`[CapacityInGb <Int32?>]`: Capacità massima (GB).</span><span class="sxs-lookup"><span data-stu-id="26f69-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="26f69-136">`[NumberOfStorageAccounts <Int32?>]`: Numero totale di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="26f69-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="26f69-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26f69-137">RELATED LINKS</span></span>

