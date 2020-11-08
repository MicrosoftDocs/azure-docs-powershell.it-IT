---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199704"
---
# <span data-ttu-id="c74be-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="c74be-101">Remove-AzImage</span></span>

## <span data-ttu-id="c74be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c74be-102">SYNOPSIS</span></span>
<span data-ttu-id="c74be-103">Rimuove un'immagine.</span><span class="sxs-lookup"><span data-stu-id="c74be-103">Removes an image.</span></span>

## <span data-ttu-id="c74be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c74be-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c74be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c74be-105">DESCRIPTION</span></span>
<span data-ttu-id="c74be-106">Il cmdlet **Remove-aziming** rimuove un'immagine.</span><span class="sxs-lookup"><span data-stu-id="c74be-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="c74be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c74be-107">EXAMPLES</span></span>

### <span data-ttu-id="c74be-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c74be-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="c74be-109">Questo comando rimuove l'immagine denominata "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c74be-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c74be-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c74be-110">PARAMETERS</span></span>

### <span data-ttu-id="c74be-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c74be-111">-AsJob</span></span>
<span data-ttu-id="c74be-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="c74be-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c74be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c74be-113">-DefaultProfile</span></span>
<span data-ttu-id="c74be-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c74be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c74be-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c74be-115">-Force</span></span>
<span data-ttu-id="c74be-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c74be-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c74be-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="c74be-117">-ImageName</span></span>
<span data-ttu-id="c74be-118">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="c74be-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c74be-119">-ResourceGroupName</span></span>
<span data-ttu-id="c74be-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c74be-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74be-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c74be-121">-Confirm</span></span>
<span data-ttu-id="c74be-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c74be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c74be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c74be-123">-WhatIf</span></span>
<span data-ttu-id="c74be-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c74be-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c74be-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c74be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c74be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74be-126">CommonParameters</span></span>
<span data-ttu-id="c74be-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c74be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74be-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c74be-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74be-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c74be-129">INPUTS</span></span>

### <span data-ttu-id="c74be-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c74be-130">System.String</span></span>

## <span data-ttu-id="c74be-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c74be-131">OUTPUTS</span></span>

### <span data-ttu-id="c74be-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c74be-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c74be-133">Note</span><span class="sxs-lookup"><span data-stu-id="c74be-133">NOTES</span></span>

## <span data-ttu-id="c74be-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c74be-134">RELATED LINKS</span></span>
