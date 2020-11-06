---
external help file: ''
Module Name: ''
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: c440fa43a4e15abb5ab9f87d5b814fe3cbc55d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512736"
---
# <span data-ttu-id="26881-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="26881-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="26881-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26881-102">SYNOPSIS</span></span>
<span data-ttu-id="26881-103">Convertire VM Hyper-V in file di disco rigido virtuali supportati in Azure</span><span class="sxs-lookup"><span data-stu-id="26881-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26881-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26881-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="26881-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26881-105">DESCRIPTION</span></span>
<span data-ttu-id="26881-106">Convertire VM Hyper-V in file di disco rigido virtuali supportati in Azure</span><span class="sxs-lookup"><span data-stu-id="26881-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="26881-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26881-107">EXAMPLES</span></span>

### <span data-ttu-id="26881-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26881-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="26881-109">Convertire VM Hyper-V denominata "test" in Azure i file del disco rigido virtuali supportati nella cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="26881-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="26881-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26881-110">PARAMETERS</span></span>

### <span data-ttu-id="26881-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26881-111">-AsJob</span></span>
<span data-ttu-id="26881-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="26881-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26881-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="26881-113">-ExportPath</span></span>
<span data-ttu-id="26881-114">Percorso della cartella di esportazione che conterrà i file del disco.</span><span class="sxs-lookup"><span data-stu-id="26881-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26881-115">-Force</span><span class="sxs-lookup"><span data-stu-id="26881-115">-Force</span></span>
<span data-ttu-id="26881-116">Forzare l'esportazione anche se viene trovata una cartella esistente.</span><span class="sxs-lookup"><span data-stu-id="26881-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26881-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="26881-117">-HyperVServer</span></span>
<span data-ttu-id="26881-118">Nome DNS del server Hyper-V con "localhost" come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="26881-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26881-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="26881-119">-HyperVVMName</span></span>
<span data-ttu-id="26881-120">Nome del nome Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="26881-120">The Hyper-V name name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26881-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26881-121">CommonParameters</span></span>
<span data-ttu-id="26881-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26881-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26881-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26881-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26881-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26881-124">INPUTS</span></span>

### <span data-ttu-id="26881-125">System. String</span><span class="sxs-lookup"><span data-stu-id="26881-125">System.String</span></span>

## <span data-ttu-id="26881-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26881-126">OUTPUTS</span></span>

### <span data-ttu-id="26881-127">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="26881-127">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="26881-128">Note</span><span class="sxs-lookup"><span data-stu-id="26881-128">NOTES</span></span>

## <span data-ttu-id="26881-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26881-129">RELATED LINKS</span></span>

