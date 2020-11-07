---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: f8da805a2c15356a4bf2188238b9a42a10617427
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866126"
---
# <span data-ttu-id="e5860-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e5860-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="e5860-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5860-102">SYNOPSIS</span></span>
<span data-ttu-id="e5860-103">Revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="e5860-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5860-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5860-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5860-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5860-105">DESCRIPTION</span></span>
<span data-ttu-id="e5860-106">Il cmdlet **Revoke-AzureRmDiskAccess** revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="e5860-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="e5860-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5860-107">EXAMPLES</span></span>

### <span data-ttu-id="e5860-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5860-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="e5860-109">Revocare l'accesso al disco denominato "Disk01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="e5860-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="e5860-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5860-110">PARAMETERS</span></span>

### <span data-ttu-id="e5860-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5860-111">-AsJob</span></span>
<span data-ttu-id="e5860-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e5860-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5860-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5860-113">-DefaultProfile</span></span>
<span data-ttu-id="e5860-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5860-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5860-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="e5860-115">-DiskName</span></span>
<span data-ttu-id="e5860-116">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="e5860-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="e5860-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5860-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5860-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5860-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e5860-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5860-119">-Confirm</span></span>
<span data-ttu-id="e5860-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5860-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5860-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5860-121">-WhatIf</span></span>
<span data-ttu-id="e5860-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5860-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5860-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5860-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5860-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5860-124">CommonParameters</span></span>
<span data-ttu-id="e5860-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5860-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5860-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5860-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5860-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5860-127">INPUTS</span></span>

### <span data-ttu-id="e5860-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e5860-128">System.String</span></span>

## <span data-ttu-id="e5860-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5860-129">OUTPUTS</span></span>

### <span data-ttu-id="e5860-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="e5860-130">System.Object</span></span>

## <span data-ttu-id="e5860-131">Note</span><span class="sxs-lookup"><span data-stu-id="e5860-131">NOTES</span></span>

## <span data-ttu-id="e5860-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5860-132">RELATED LINKS</span></span>

