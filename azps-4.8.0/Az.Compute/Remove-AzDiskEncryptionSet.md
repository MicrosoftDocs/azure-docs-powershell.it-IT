---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033259"
---
# <span data-ttu-id="a317b-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a317b-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="a317b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a317b-102">SYNOPSIS</span></span>
<span data-ttu-id="a317b-103">Rimuove un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="a317b-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="a317b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a317b-104">SYNTAX</span></span>

### <span data-ttu-id="a317b-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a317b-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a317b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a317b-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a317b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a317b-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a317b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a317b-108">DESCRIPTION</span></span>
<span data-ttu-id="a317b-109">Rimuove un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="a317b-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="a317b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a317b-110">EXAMPLES</span></span>

### <span data-ttu-id="a317b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a317b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="a317b-112">Eliminare il set di crittografia disco "ENC1" in "RG1"</span><span class="sxs-lookup"><span data-stu-id="a317b-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="a317b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a317b-113">PARAMETERS</span></span>

### <span data-ttu-id="a317b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a317b-114">-AsJob</span></span>
<span data-ttu-id="a317b-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a317b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a317b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a317b-116">-DefaultProfile</span></span>
<span data-ttu-id="a317b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a317b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a317b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a317b-118">-Force</span></span>
<span data-ttu-id="a317b-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a317b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a317b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a317b-120">-InputObject</span></span>
<span data-ttu-id="a317b-121">Oggetto local del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="a317b-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="a317b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a317b-122">-Name</span></span>
<span data-ttu-id="a317b-123">Nome del set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="a317b-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="a317b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a317b-124">-ResourceGroupName</span></span>
<span data-ttu-id="a317b-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a317b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a317b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a317b-126">-ResourceId</span></span>
<span data-ttu-id="a317b-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a317b-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="a317b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a317b-128">-Confirm</span></span>
<span data-ttu-id="a317b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a317b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a317b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a317b-130">-WhatIf</span></span>
<span data-ttu-id="a317b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a317b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a317b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a317b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a317b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a317b-133">CommonParameters</span></span>
<span data-ttu-id="a317b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a317b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a317b-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a317b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a317b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a317b-136">INPUTS</span></span>

### <span data-ttu-id="a317b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a317b-137">System.String</span></span>

### <span data-ttu-id="a317b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a317b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="a317b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a317b-139">OUTPUTS</span></span>

### <span data-ttu-id="a317b-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a317b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a317b-141">Note</span><span class="sxs-lookup"><span data-stu-id="a317b-141">NOTES</span></span>

## <span data-ttu-id="a317b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a317b-142">RELATED LINKS</span></span>
