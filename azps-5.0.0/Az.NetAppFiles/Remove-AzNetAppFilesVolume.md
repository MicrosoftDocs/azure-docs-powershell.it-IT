---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201848"
---
# <span data-ttu-id="f7375-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f7375-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f7375-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7375-102">SYNOPSIS</span></span>
<span data-ttu-id="f7375-103">Elimina un volume di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="f7375-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="f7375-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7375-104">SYNTAX</span></span>

### <span data-ttu-id="f7375-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7375-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7375-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7375-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7375-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7375-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7375-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7375-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7375-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7375-109">DESCRIPTION</span></span>
<span data-ttu-id="f7375-110">Il cmdlet **Remove-AzNetAppFilesVolume** Elimina un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="f7375-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="f7375-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7375-111">EXAMPLES</span></span>

### <span data-ttu-id="f7375-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7375-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="f7375-113">Questo comando Elimina il volume ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="f7375-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="f7375-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7375-114">PARAMETERS</span></span>

### <span data-ttu-id="f7375-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7375-115">-AccountName</span></span>
<span data-ttu-id="f7375-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="f7375-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f7375-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7375-117">-DefaultProfile</span></span>
<span data-ttu-id="f7375-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7375-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7375-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7375-119">-InputObject</span></span>
<span data-ttu-id="f7375-120">Oggetto volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f7375-120">The volume object to remove</span></span>

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

### <span data-ttu-id="f7375-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7375-121">-Name</span></span>
<span data-ttu-id="f7375-122">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="f7375-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f7375-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7375-123">-PassThru</span></span>
<span data-ttu-id="f7375-124">Restituirà se il volume specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="f7375-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="f7375-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f7375-125">-PoolName</span></span>
<span data-ttu-id="f7375-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="f7375-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f7375-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="f7375-127">-PoolObject</span></span>
<span data-ttu-id="f7375-128">Oggetto pool contenente il volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f7375-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="f7375-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7375-129">-ResourceGroupName</span></span>
<span data-ttu-id="f7375-130">Gruppo risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="f7375-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="f7375-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7375-131">-ResourceId</span></span>
<span data-ttu-id="f7375-132">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="f7375-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="f7375-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7375-133">-Confirm</span></span>
<span data-ttu-id="f7375-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7375-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7375-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7375-135">-WhatIf</span></span>
<span data-ttu-id="f7375-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7375-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7375-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7375-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7375-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7375-138">CommonParameters</span></span>
<span data-ttu-id="f7375-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7375-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7375-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7375-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7375-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7375-141">INPUTS</span></span>

### <span data-ttu-id="f7375-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f7375-142">System.String</span></span>

### <span data-ttu-id="f7375-143">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f7375-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="f7375-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f7375-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f7375-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7375-145">OUTPUTS</span></span>

### <span data-ttu-id="f7375-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7375-146">System.Boolean</span></span>

## <span data-ttu-id="f7375-147">Note</span><span class="sxs-lookup"><span data-stu-id="f7375-147">NOTES</span></span>

## <span data-ttu-id="f7375-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7375-148">RELATED LINKS</span></span>
