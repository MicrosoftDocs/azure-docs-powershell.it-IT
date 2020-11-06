---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: 2787c1cf8a37fd5d143e95c55d3e98b625d4d82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509991"
---
# <span data-ttu-id="13e11-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="13e11-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="13e11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13e11-102">SYNOPSIS</span></span>
<span data-ttu-id="13e11-103">Concede un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="13e11-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13e11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13e11-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13e11-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13e11-105">DESCRIPTION</span></span>
<span data-ttu-id="13e11-106">Il cmdlet **Grant-AzureRmDiskAccess** concede un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="13e11-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="13e11-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13e11-107">EXAMPLES</span></span>

### <span data-ttu-id="13e11-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13e11-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="13e11-109">Concedere l'accesso "Leggi" al disco denominato "Disk01" nel gruppo risorse denominato "ResourceGroup01" per 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="13e11-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="13e11-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13e11-110">PARAMETERS</span></span>

### <span data-ttu-id="13e11-111">-Access</span><span class="sxs-lookup"><span data-stu-id="13e11-111">-Access</span></span>
<span data-ttu-id="13e11-112">Specifica il livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="13e11-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e11-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="13e11-113">-DiskName</span></span>
<span data-ttu-id="13e11-114">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="13e11-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="13e11-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="13e11-115">-DurationInSecond</span></span>
<span data-ttu-id="13e11-116">Specifica la durata di accesso in secondi.</span><span class="sxs-lookup"><span data-stu-id="13e11-116">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e11-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13e11-117">-ResourceGroupName</span></span>
<span data-ttu-id="13e11-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13e11-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="13e11-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="13e11-119">-Confirm</span></span>
<span data-ttu-id="13e11-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13e11-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e11-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e11-121">-WhatIf</span></span>
<span data-ttu-id="13e11-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13e11-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13e11-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13e11-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e11-124">CommonParameters</span></span>
<span data-ttu-id="13e11-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13e11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e11-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e11-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e11-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13e11-127">INPUTS</span></span>

### <span data-ttu-id="13e11-128">System. String</span><span class="sxs-lookup"><span data-stu-id="13e11-128">System.String</span></span>

## <span data-ttu-id="13e11-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13e11-129">OUTPUTS</span></span>

### <span data-ttu-id="13e11-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="13e11-130">System.Object</span></span>

## <span data-ttu-id="13e11-131">Note</span><span class="sxs-lookup"><span data-stu-id="13e11-131">NOTES</span></span>

## <span data-ttu-id="13e11-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13e11-132">RELATED LINKS</span></span>

