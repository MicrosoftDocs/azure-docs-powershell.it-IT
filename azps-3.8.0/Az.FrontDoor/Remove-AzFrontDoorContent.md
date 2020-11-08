---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018664"
---
# <span data-ttu-id="96e74-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="96e74-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="96e74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96e74-102">SYNOPSIS</span></span>
<span data-ttu-id="96e74-103">Rimuovere il contenuto nello sportello anteriore</span><span class="sxs-lookup"><span data-stu-id="96e74-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="96e74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96e74-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96e74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96e74-105">DESCRIPTION</span></span>
<span data-ttu-id="96e74-106">Remove-AzFrontDoorContent Elimina il contenuto memorizzato nella cache in uno sportello anteriore</span><span class="sxs-lookup"><span data-stu-id="96e74-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="96e74-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96e74-107">EXAMPLES</span></span>

### <span data-ttu-id="96e74-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96e74-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="96e74-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96e74-109">PARAMETERS</span></span>

### <span data-ttu-id="96e74-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="96e74-110">-ContentPath</span></span>
<span data-ttu-id="96e74-111">Percorsi per il contenuto da eliminare.</span><span class="sxs-lookup"><span data-stu-id="96e74-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e74-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e74-112">-DefaultProfile</span></span>
<span data-ttu-id="96e74-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96e74-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96e74-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="96e74-114">-Name</span></span>
<span data-ttu-id="96e74-115">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="96e74-115">Front Door name.</span></span>

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

### <span data-ttu-id="96e74-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96e74-116">-PassThru</span></span>
<span data-ttu-id="96e74-117">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="96e74-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="96e74-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e74-118">-ResourceGroupName</span></span>
<span data-ttu-id="96e74-119">Nome del gruppo di risorse dello sportello anteriore</span><span class="sxs-lookup"><span data-stu-id="96e74-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="96e74-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="96e74-120">-Confirm</span></span>
<span data-ttu-id="96e74-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e74-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e74-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e74-122">-WhatIf</span></span>
<span data-ttu-id="96e74-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96e74-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96e74-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96e74-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e74-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e74-125">CommonParameters</span></span>
<span data-ttu-id="96e74-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e74-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e74-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96e74-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e74-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96e74-128">INPUTS</span></span>

### <span data-ttu-id="96e74-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="96e74-129">None</span></span>

## <span data-ttu-id="96e74-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96e74-130">OUTPUTS</span></span>

### <span data-ttu-id="96e74-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96e74-131">System.Boolean</span></span>

## <span data-ttu-id="96e74-132">Note</span><span class="sxs-lookup"><span data-stu-id="96e74-132">NOTES</span></span>

## <span data-ttu-id="96e74-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96e74-133">RELATED LINKS</span></span>
