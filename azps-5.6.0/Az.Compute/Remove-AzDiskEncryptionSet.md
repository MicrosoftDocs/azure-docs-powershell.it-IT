---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: ec146441e620580b5028dffa4e0f7f3e09c45b35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988369"
---
# <span data-ttu-id="dd42f-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="dd42f-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="dd42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd42f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd42f-103">Rimuove un set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="dd42f-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="dd42f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd42f-104">SYNTAX</span></span>

### <span data-ttu-id="dd42f-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="dd42f-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd42f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="dd42f-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd42f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="dd42f-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd42f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd42f-108">DESCRIPTION</span></span>
<span data-ttu-id="dd42f-109">Rimuove un set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="dd42f-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="dd42f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd42f-110">EXAMPLES</span></span>

### <span data-ttu-id="dd42f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd42f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="dd42f-112">Eliminare il set di crittografia disco 'enc1' in 'rg1'</span><span class="sxs-lookup"><span data-stu-id="dd42f-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="dd42f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd42f-113">PARAMETERS</span></span>

### <span data-ttu-id="dd42f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd42f-114">-AsJob</span></span>
<span data-ttu-id="dd42f-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dd42f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd42f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd42f-116">-DefaultProfile</span></span>
<span data-ttu-id="dd42f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd42f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd42f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dd42f-118">-Force</span></span>
<span data-ttu-id="dd42f-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="dd42f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dd42f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd42f-120">-InputObject</span></span>
<span data-ttu-id="dd42f-121">Oggetto locale del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="dd42f-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd42f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dd42f-122">-Name</span></span>
<span data-ttu-id="dd42f-123">Nome del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="dd42f-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd42f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd42f-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd42f-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd42f-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd42f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd42f-126">-ResourceId</span></span>
<span data-ttu-id="dd42f-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd42f-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd42f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd42f-128">-Confirm</span></span>
<span data-ttu-id="dd42f-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd42f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd42f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd42f-130">-WhatIf</span></span>
<span data-ttu-id="dd42f-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd42f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd42f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd42f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd42f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd42f-133">CommonParameters</span></span>
<span data-ttu-id="dd42f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd42f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd42f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd42f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd42f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd42f-136">INPUTS</span></span>

### <span data-ttu-id="dd42f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="dd42f-137">System.String</span></span>

### <span data-ttu-id="dd42f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="dd42f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="dd42f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd42f-139">OUTPUTS</span></span>

### <span data-ttu-id="dd42f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="dd42f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="dd42f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd42f-141">NOTES</span></span>

## <span data-ttu-id="dd42f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd42f-142">RELATED LINKS</span></span>
