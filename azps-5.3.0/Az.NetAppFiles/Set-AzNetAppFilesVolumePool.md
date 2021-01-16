---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380505"
---
# <span data-ttu-id="7f7cd-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="7f7cd-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="7f7cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7cd-103">Cambiare il pool per un volume di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="7f7cd-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="7f7cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f7cd-104">SYNTAX</span></span>

### <span data-ttu-id="7f7cd-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f7cd-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f7cd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7cd-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f7cd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7cd-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f7cd-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7cd-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f7cd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f7cd-109">DESCRIPTION</span></span>
<span data-ttu-id="7f7cd-110">Il cmdlet **set-AzNetAppFilesVolumePool** modifica il pool di un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="7f7cd-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="7f7cd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f7cd-111">EXAMPLES</span></span>

### <span data-ttu-id="7f7cd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7f7cd-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="7f7cd-113">In questo articolo viene modificato il pool di volumi volume su uno con l'ID di 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="7f7cd-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="7f7cd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f7cd-114">PARAMETERS</span></span>

### <span data-ttu-id="7f7cd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7f7cd-115">-AccountName</span></span>
<span data-ttu-id="7f7cd-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="7f7cd-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f7cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7cd-117">-DefaultProfile</span></span>
<span data-ttu-id="7f7cd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f7cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f7cd-119">-InputObject</span></span>
<span data-ttu-id="7f7cd-120">Oggetto volume da trasferire</span><span class="sxs-lookup"><span data-stu-id="7f7cd-120">The volume object to move</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f7cd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f7cd-121">-Name</span></span>
<span data-ttu-id="7f7cd-122">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="7f7cd-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f7cd-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="7f7cd-123">-NewPoolResourceId</span></span>
<span data-ttu-id="7f7cd-124">ResourceId del pool di capacità in cui trasferirsi.</span><span class="sxs-lookup"><span data-stu-id="7f7cd-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="7f7cd-125">UUID V4 usato per identificare il pool</span><span class="sxs-lookup"><span data-stu-id="7f7cd-125">UUID v4 used to identify the pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f7cd-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7f7cd-126">-PoolName</span></span>
<span data-ttu-id="7f7cd-127">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="7f7cd-127">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f7cd-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="7f7cd-128">-PoolObject</span></span>
<span data-ttu-id="7f7cd-129">Oggetto pool contenente il volume</span><span class="sxs-lookup"><span data-stu-id="7f7cd-129">The pool object containing the volume</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f7cd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7cd-130">-ResourceGroupName</span></span>
<span data-ttu-id="7f7cd-131">Gruppo risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="7f7cd-131">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f7cd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f7cd-132">-ResourceId</span></span>
<span data-ttu-id="7f7cd-133">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="7f7cd-133">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f7cd-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f7cd-134">-Confirm</span></span>
<span data-ttu-id="7f7cd-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f7cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f7cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f7cd-136">-WhatIf</span></span>
<span data-ttu-id="7f7cd-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f7cd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f7cd-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f7cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f7cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7cd-139">CommonParameters</span></span>
<span data-ttu-id="7f7cd-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7cd-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f7cd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7cd-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f7cd-142">INPUTS</span></span>

### <span data-ttu-id="7f7cd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7f7cd-143">System.String</span></span>

### <span data-ttu-id="7f7cd-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7f7cd-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="7f7cd-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7f7cd-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7f7cd-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f7cd-146">OUTPUTS</span></span>

### <span data-ttu-id="7f7cd-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f7cd-147">System.Boolean</span></span>

## <span data-ttu-id="7f7cd-148">Note</span><span class="sxs-lookup"><span data-stu-id="7f7cd-148">NOTES</span></span>

## <span data-ttu-id="7f7cd-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f7cd-149">RELATED LINKS</span></span>
