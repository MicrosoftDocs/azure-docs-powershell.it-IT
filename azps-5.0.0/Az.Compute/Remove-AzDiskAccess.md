---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193680"
---
# <span data-ttu-id="a2762-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a2762-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="a2762-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2762-102">SYNOPSIS</span></span>
<span data-ttu-id="a2762-103">Rimuove una risorsa di accesso al disco.</span><span class="sxs-lookup"><span data-stu-id="a2762-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="a2762-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2762-104">SYNTAX</span></span>

### <span data-ttu-id="a2762-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2762-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2762-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2762-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2762-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2762-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2762-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2762-108">DESCRIPTION</span></span>
<span data-ttu-id="a2762-109">Il cmdlet **Remove-AzDiskAccess** rimuove una risorsa di Access su disco.</span><span class="sxs-lookup"><span data-stu-id="a2762-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="a2762-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2762-110">EXAMPLES</span></span>

### <span data-ttu-id="a2762-111">Esempio 1: rimuovere l'accesso al disco usando il set di parametri predefinito</span><span class="sxs-lookup"><span data-stu-id="a2762-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="a2762-112">Questo comando rimuove l'accesso al disco denominato "DiskAccess01" nel gruppo di risorse "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="a2762-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="a2762-113">Esempio 2: rimuovere l'accesso al disco tramite ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a2762-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="a2762-114">Questo comando rimuove l'accesso al disco tramite ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a2762-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="a2762-115">Esempio 3: rimuovere l'accesso al disco usando l'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="a2762-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="a2762-116">Questo comando rimuove l'accesso al disco da InputObject</span><span class="sxs-lookup"><span data-stu-id="a2762-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="a2762-117">Esempio 4: rimuovere l'accesso al disco tramite l'oggetto di input piping</span><span class="sxs-lookup"><span data-stu-id="a2762-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="a2762-118">Questo comando rimuove l'accesso al disco eseguendo il piping di InputObject</span><span class="sxs-lookup"><span data-stu-id="a2762-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="a2762-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2762-119">PARAMETERS</span></span>

### <span data-ttu-id="a2762-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2762-120">-AsJob</span></span>
<span data-ttu-id="a2762-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a2762-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2762-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2762-122">-DefaultProfile</span></span>
<span data-ttu-id="a2762-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2762-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2762-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2762-124">-InputObject</span></span>
<span data-ttu-id="a2762-125">Oggetto di Access su disco di PowerShell</span><span class="sxs-lookup"><span data-stu-id="a2762-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2762-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2762-126">-Name</span></span>
<span data-ttu-id="a2762-127">Specifica il nome di un accesso su disco.</span><span class="sxs-lookup"><span data-stu-id="a2762-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2762-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2762-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2762-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2762-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2762-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2762-130">-ResourceId</span></span>
<span data-ttu-id="a2762-131">ID risorsa per l'accesso al disco.</span><span class="sxs-lookup"><span data-stu-id="a2762-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2762-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2762-132">-Confirm</span></span>
<span data-ttu-id="a2762-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2762-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2762-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2762-134">-WhatIf</span></span>
<span data-ttu-id="a2762-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2762-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2762-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2762-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2762-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2762-137">CommonParameters</span></span>
<span data-ttu-id="a2762-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2762-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2762-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2762-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2762-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2762-140">INPUTS</span></span>

### <span data-ttu-id="a2762-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a2762-141">System.String</span></span>

### <span data-ttu-id="a2762-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a2762-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="a2762-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2762-143">OUTPUTS</span></span>

### <span data-ttu-id="a2762-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a2762-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a2762-145">Note</span><span class="sxs-lookup"><span data-stu-id="a2762-145">NOTES</span></span>

## <span data-ttu-id="a2762-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2762-146">RELATED LINKS</span></span>