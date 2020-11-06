---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 7d6d130f639265cd2b7e2885f117d2e29899b8c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521258"
---
# <span data-ttu-id="4383b-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="4383b-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="4383b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4383b-102">SYNOPSIS</span></span>
<span data-ttu-id="4383b-103">Rimuove un'immagine.</span><span class="sxs-lookup"><span data-stu-id="4383b-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4383b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4383b-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4383b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4383b-105">DESCRIPTION</span></span>
<span data-ttu-id="4383b-106">Il cmdlet **Remove-AzureRmImage** rimuove un'immagine.</span><span class="sxs-lookup"><span data-stu-id="4383b-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="4383b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4383b-107">EXAMPLES</span></span>

### <span data-ttu-id="4383b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4383b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="4383b-109">Questo comando rimuove l'immagine denominata "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="4383b-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4383b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4383b-110">PARAMETERS</span></span>

### <span data-ttu-id="4383b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4383b-111">-DefaultProfile</span></span>
<span data-ttu-id="4383b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4383b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4383b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4383b-113">-Force</span></span>
<span data-ttu-id="4383b-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4383b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4383b-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="4383b-115">-ImageName</span></span>
<span data-ttu-id="4383b-116">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="4383b-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4383b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4383b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4383b-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4383b-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4383b-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4383b-119">-Confirm</span></span>
<span data-ttu-id="4383b-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4383b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4383b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4383b-121">-WhatIf</span></span>
<span data-ttu-id="4383b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4383b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4383b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4383b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4383b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4383b-124">CommonParameters</span></span>
<span data-ttu-id="4383b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4383b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4383b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4383b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4383b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4383b-127">INPUTS</span></span>

### <span data-ttu-id="4383b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4383b-128">System.String</span></span>

## <span data-ttu-id="4383b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4383b-129">OUTPUTS</span></span>

### <span data-ttu-id="4383b-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="4383b-130">System.Object</span></span>

## <span data-ttu-id="4383b-131">Note</span><span class="sxs-lookup"><span data-stu-id="4383b-131">NOTES</span></span>

## <span data-ttu-id="4383b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4383b-132">RELATED LINKS</span></span>

