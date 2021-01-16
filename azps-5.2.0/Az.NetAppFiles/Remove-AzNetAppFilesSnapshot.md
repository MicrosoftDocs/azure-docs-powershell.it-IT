---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345211"
---
# <span data-ttu-id="86566-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="86566-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="86566-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86566-102">SYNOPSIS</span></span>
<span data-ttu-id="86566-103">Elimina uno snapshot di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="86566-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="86566-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86566-104">SYNTAX</span></span>

### <span data-ttu-id="86566-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86566-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86566-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86566-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86566-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86566-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86566-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86566-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86566-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86566-109">DESCRIPTION</span></span>
<span data-ttu-id="86566-110">Il cmdlet **Remove-AzNetAppFilesSnapshot** Elimina uno snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="86566-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="86566-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86566-111">EXAMPLES</span></span>

### <span data-ttu-id="86566-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86566-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="86566-113">Questo comando Elimina lo snapshot ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="86566-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="86566-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86566-114">PARAMETERS</span></span>

### <span data-ttu-id="86566-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="86566-115">-AccountName</span></span>
<span data-ttu-id="86566-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="86566-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="86566-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86566-117">-DefaultProfile</span></span>
<span data-ttu-id="86566-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86566-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86566-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86566-119">-InputObject</span></span>
<span data-ttu-id="86566-120">Oggetto snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="86566-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86566-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="86566-121">-Name</span></span>
<span data-ttu-id="86566-122">Nome dello snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="86566-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86566-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86566-123">-PassThru</span></span>
<span data-ttu-id="86566-124">Restituirà se il volume specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="86566-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="86566-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="86566-125">-PoolName</span></span>
<span data-ttu-id="86566-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="86566-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="86566-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86566-127">-ResourceGroupName</span></span>
<span data-ttu-id="86566-128">Gruppo di risorse dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="86566-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="86566-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86566-129">-ResourceId</span></span>
<span data-ttu-id="86566-130">ID risorsa dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="86566-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="86566-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="86566-131">-VolumeName</span></span>
<span data-ttu-id="86566-132">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="86566-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="86566-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="86566-133">-VolumeObject</span></span>
<span data-ttu-id="86566-134">Oggetto volume che contiene lo snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="86566-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86566-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86566-135">-Confirm</span></span>
<span data-ttu-id="86566-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86566-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86566-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86566-137">-WhatIf</span></span>
<span data-ttu-id="86566-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86566-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86566-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86566-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86566-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86566-140">CommonParameters</span></span>
<span data-ttu-id="86566-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86566-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86566-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86566-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86566-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86566-143">INPUTS</span></span>

### <span data-ttu-id="86566-144">System. String</span><span class="sxs-lookup"><span data-stu-id="86566-144">System.String</span></span>

### <span data-ttu-id="86566-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="86566-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="86566-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="86566-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="86566-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86566-147">OUTPUTS</span></span>

### <span data-ttu-id="86566-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86566-148">System.Boolean</span></span>

## <span data-ttu-id="86566-149">Note</span><span class="sxs-lookup"><span data-stu-id="86566-149">NOTES</span></span>

## <span data-ttu-id="86566-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86566-150">RELATED LINKS</span></span>
