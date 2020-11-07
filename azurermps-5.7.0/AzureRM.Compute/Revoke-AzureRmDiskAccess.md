---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521080"
---
# <span data-ttu-id="e65f6-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e65f6-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="e65f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e65f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e65f6-103">Revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="e65f6-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e65f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e65f6-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e65f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e65f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e65f6-106">Il cmdlet **Revoke-AzureRmDiskAccess** revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="e65f6-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="e65f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e65f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e65f6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e65f6-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="e65f6-109">Revocare l'accesso al disco denominato "Disk01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="e65f6-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="e65f6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e65f6-110">PARAMETERS</span></span>

### <span data-ttu-id="e65f6-111">-Diskname</span><span class="sxs-lookup"><span data-stu-id="e65f6-111">-DiskName</span></span>
<span data-ttu-id="e65f6-112">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="e65f6-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="e65f6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e65f6-113">-ResourceGroupName</span></span>
<span data-ttu-id="e65f6-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e65f6-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e65f6-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e65f6-115">-Confirm</span></span>
<span data-ttu-id="e65f6-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e65f6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e65f6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e65f6-117">-WhatIf</span></span>
<span data-ttu-id="e65f6-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e65f6-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e65f6-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e65f6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e65f6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e65f6-120">CommonParameters</span></span>
<span data-ttu-id="e65f6-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e65f6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e65f6-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e65f6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e65f6-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e65f6-123">INPUTS</span></span>

### <span data-ttu-id="e65f6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e65f6-124">System.String</span></span>

## <span data-ttu-id="e65f6-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e65f6-125">OUTPUTS</span></span>

### <span data-ttu-id="e65f6-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="e65f6-126">System.Object</span></span>

## <span data-ttu-id="e65f6-127">Note</span><span class="sxs-lookup"><span data-stu-id="e65f6-127">NOTES</span></span>

## <span data-ttu-id="e65f6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e65f6-128">RELATED LINKS</span></span>
