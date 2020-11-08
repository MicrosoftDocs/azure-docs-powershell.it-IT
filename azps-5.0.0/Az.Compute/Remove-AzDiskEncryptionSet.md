---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201404"
---
# <span data-ttu-id="b3bb4-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b3bb4-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="b3bb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bb4-103">Rimuove un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="b3bb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3bb4-104">SYNTAX</span></span>

### <span data-ttu-id="b3bb4-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3bb4-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3bb4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b3bb4-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3bb4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b3bb4-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3bb4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3bb4-108">DESCRIPTION</span></span>
<span data-ttu-id="b3bb4-109">Rimuove un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="b3bb4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3bb4-110">EXAMPLES</span></span>

### <span data-ttu-id="b3bb4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3bb4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="b3bb4-112">Eliminare il set di crittografia disco "ENC1" in "RG1"</span><span class="sxs-lookup"><span data-stu-id="b3bb4-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="b3bb4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3bb4-113">PARAMETERS</span></span>

### <span data-ttu-id="b3bb4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3bb4-114">-AsJob</span></span>
<span data-ttu-id="b3bb4-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b3bb4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3bb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bb4-116">-DefaultProfile</span></span>
<span data-ttu-id="b3bb4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3bb4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b3bb4-118">-Force</span></span>
<span data-ttu-id="b3bb4-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3bb4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3bb4-120">-InputObject</span></span>
<span data-ttu-id="b3bb4-121">Oggetto local del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="b3bb4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3bb4-122">-Name</span></span>
<span data-ttu-id="b3bb4-123">Nome del set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="b3bb4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3bb4-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3bb4-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b3bb4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3bb4-126">-ResourceId</span></span>
<span data-ttu-id="b3bb4-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="b3bb4-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3bb4-128">-Confirm</span></span>
<span data-ttu-id="b3bb4-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3bb4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3bb4-130">-WhatIf</span></span>
<span data-ttu-id="b3bb4-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3bb4-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3bb4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bb4-133">CommonParameters</span></span>
<span data-ttu-id="b3bb4-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bb4-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3bb4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bb4-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3bb4-136">INPUTS</span></span>

### <span data-ttu-id="b3bb4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b3bb4-137">System.String</span></span>

### <span data-ttu-id="b3bb4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b3bb4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="b3bb4-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3bb4-139">OUTPUTS</span></span>

### <span data-ttu-id="b3bb4-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b3bb4-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b3bb4-141">Note</span><span class="sxs-lookup"><span data-stu-id="b3bb4-141">NOTES</span></span>

## <span data-ttu-id="b3bb4-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3bb4-142">RELATED LINKS</span></span>
