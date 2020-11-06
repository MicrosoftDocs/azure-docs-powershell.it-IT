---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509296"
---
# <span data-ttu-id="e9f4b-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="e9f4b-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="e9f4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f4b-103">Convertire VM Hyper-V in file di disco rigido virtuali supportati in Azure</span><span class="sxs-lookup"><span data-stu-id="e9f4b-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9f4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9f4b-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9f4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="e9f4b-106">Convertire VM Hyper-V in file di disco rigido virtuali supportati in Azure</span><span class="sxs-lookup"><span data-stu-id="e9f4b-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="e9f4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9f4b-107">EXAMPLES</span></span>

### <span data-ttu-id="e9f4b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9f4b-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="e9f4b-109">Convertire VM Hyper-V denominata "test" in Azure i file del disco rigido virtuali supportati nella cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="e9f4b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9f4b-110">PARAMETERS</span></span>

### <span data-ttu-id="e9f4b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9f4b-111">-AsJob</span></span>
<span data-ttu-id="e9f4b-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e9f4b-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="e9f4b-113">-ExportPath</span></span>
<span data-ttu-id="e9f4b-114">Percorso della cartella di esportazione che conterrà i file del disco.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f4b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e9f4b-115">-Force</span></span>
<span data-ttu-id="e9f4b-116">Forzare l'esportazione anche se viene trovata una cartella esistente.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f4b-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="e9f4b-117">-HyperVServer</span></span>
<span data-ttu-id="e9f4b-118">Nome DNS del server Hyper-V con "localhost" come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f4b-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="e9f4b-119">-HyperVVMName</span></span>
<span data-ttu-id="e9f4b-120">Nome del nome Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f4b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e9f4b-121">-Confirm</span></span>
<span data-ttu-id="e9f4b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f4b-123">-WhatIf</span></span>
<span data-ttu-id="e9f4b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9f4b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f4b-126">CommonParameters</span></span>
<span data-ttu-id="e9f4b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f4b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f4b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f4b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9f4b-129">INPUTS</span></span>

### <span data-ttu-id="e9f4b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f4b-130">System.String</span></span>

## <span data-ttu-id="e9f4b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9f4b-131">OUTPUTS</span></span>

### <span data-ttu-id="e9f4b-132">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="e9f4b-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="e9f4b-133">Note</span><span class="sxs-lookup"><span data-stu-id="e9f4b-133">NOTES</span></span>

## <span data-ttu-id="e9f4b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9f4b-134">RELATED LINKS</span></span>
