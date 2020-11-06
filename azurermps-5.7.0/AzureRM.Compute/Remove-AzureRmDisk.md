---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 10150d7941aa3b17a0a7d4447ff0a57e3d04a516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509972"
---
# <span data-ttu-id="0c11a-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0c11a-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="0c11a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c11a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c11a-103">Rimuove un disco.</span><span class="sxs-lookup"><span data-stu-id="0c11a-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c11a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c11a-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c11a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c11a-105">DESCRIPTION</span></span>
<span data-ttu-id="0c11a-106">Il cmdlet **Remove-AzureRmDisk** rimuove un disco.</span><span class="sxs-lookup"><span data-stu-id="0c11a-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="0c11a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c11a-107">EXAMPLES</span></span>

### <span data-ttu-id="0c11a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c11a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="0c11a-109">Questo comando rimuove il disco denominato "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0c11a-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0c11a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c11a-110">PARAMETERS</span></span>

### <span data-ttu-id="0c11a-111">-Diskname</span><span class="sxs-lookup"><span data-stu-id="0c11a-111">-DiskName</span></span>
<span data-ttu-id="0c11a-112">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="0c11a-112">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c11a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0c11a-113">-Force</span></span>
<span data-ttu-id="0c11a-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c11a-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c11a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c11a-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c11a-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c11a-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c11a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c11a-117">-Confirm</span></span>
<span data-ttu-id="0c11a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c11a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c11a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c11a-119">-WhatIf</span></span>
<span data-ttu-id="0c11a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c11a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c11a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c11a-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c11a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c11a-122">CommonParameters</span></span>
<span data-ttu-id="0c11a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c11a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c11a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c11a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c11a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c11a-125">INPUTS</span></span>

### <span data-ttu-id="0c11a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0c11a-126">System.String</span></span>

## <span data-ttu-id="0c11a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c11a-127">OUTPUTS</span></span>

### <span data-ttu-id="0c11a-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="0c11a-128">System.Object</span></span>

## <span data-ttu-id="0c11a-129">Note</span><span class="sxs-lookup"><span data-stu-id="0c11a-129">NOTES</span></span>

## <span data-ttu-id="0c11a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c11a-130">RELATED LINKS</span></span>

