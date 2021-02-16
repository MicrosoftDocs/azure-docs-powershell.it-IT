---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204859"
---
# <span data-ttu-id="d9583-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d9583-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="d9583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9583-102">SYNOPSIS</span></span>
<span data-ttu-id="d9583-103">Rimuove un set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="d9583-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="d9583-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9583-104">SYNTAX</span></span>

### <span data-ttu-id="d9583-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="d9583-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9583-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d9583-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9583-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d9583-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9583-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9583-108">DESCRIPTION</span></span>
<span data-ttu-id="d9583-109">Rimuove un set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="d9583-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="d9583-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9583-110">EXAMPLES</span></span>

### <span data-ttu-id="d9583-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9583-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="d9583-112">Eliminare il set di crittografia disco 'enc1' in 'rg1'</span><span class="sxs-lookup"><span data-stu-id="d9583-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="d9583-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9583-113">PARAMETERS</span></span>

### <span data-ttu-id="d9583-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9583-114">-AsJob</span></span>
<span data-ttu-id="d9583-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d9583-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9583-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9583-116">-DefaultProfile</span></span>
<span data-ttu-id="d9583-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9583-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9583-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d9583-118">-Force</span></span>
<span data-ttu-id="d9583-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="d9583-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9583-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9583-120">-InputObject</span></span>
<span data-ttu-id="d9583-121">Oggetto locale del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="d9583-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="d9583-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d9583-122">-Name</span></span>
<span data-ttu-id="d9583-123">Nome del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="d9583-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="d9583-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9583-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9583-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9583-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d9583-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9583-126">-ResourceId</span></span>
<span data-ttu-id="d9583-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d9583-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="d9583-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9583-128">-Confirm</span></span>
<span data-ttu-id="d9583-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9583-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9583-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9583-130">-WhatIf</span></span>
<span data-ttu-id="d9583-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9583-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9583-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9583-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9583-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9583-133">CommonParameters</span></span>
<span data-ttu-id="d9583-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9583-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9583-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9583-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9583-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9583-136">INPUTS</span></span>

### <span data-ttu-id="d9583-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d9583-137">System.String</span></span>

### <span data-ttu-id="d9583-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d9583-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="d9583-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9583-139">OUTPUTS</span></span>

### <span data-ttu-id="d9583-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d9583-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d9583-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9583-141">NOTES</span></span>

## <span data-ttu-id="d9583-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9583-142">RELATED LINKS</span></span>
