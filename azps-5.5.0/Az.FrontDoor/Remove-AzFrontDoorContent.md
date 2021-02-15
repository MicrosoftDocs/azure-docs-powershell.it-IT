---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204051"
---
# <span data-ttu-id="26558-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="26558-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="26558-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26558-102">SYNOPSIS</span></span>
<span data-ttu-id="26558-103">Rimuovere il contenuto in Porta anteriore</span><span class="sxs-lookup"><span data-stu-id="26558-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="26558-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26558-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26558-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26558-105">DESCRIPTION</span></span>
<span data-ttu-id="26558-106">Remove-AzFrontDoorContent ripulire il contenuto memorizzato nella cache in una porta anteriore</span><span class="sxs-lookup"><span data-stu-id="26558-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="26558-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26558-107">EXAMPLES</span></span>

### <span data-ttu-id="26558-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26558-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="26558-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26558-109">PARAMETERS</span></span>

### <span data-ttu-id="26558-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="26558-110">-ContentPath</span></span>
<span data-ttu-id="26558-111">Percorsi del contenuto da eliminare.</span><span class="sxs-lookup"><span data-stu-id="26558-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="26558-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26558-112">-DefaultProfile</span></span>
<span data-ttu-id="26558-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26558-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26558-114">-Name</span><span class="sxs-lookup"><span data-stu-id="26558-114">-Name</span></span>
<span data-ttu-id="26558-115">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="26558-115">Front Door name.</span></span>

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

### <span data-ttu-id="26558-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26558-116">-PassThru</span></span>
<span data-ttu-id="26558-117">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="26558-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="26558-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26558-118">-ResourceGroupName</span></span>
<span data-ttu-id="26558-119">Nome del gruppo di risorse della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="26558-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="26558-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26558-120">-Confirm</span></span>
<span data-ttu-id="26558-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26558-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26558-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26558-122">-WhatIf</span></span>
<span data-ttu-id="26558-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26558-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26558-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26558-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26558-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26558-125">CommonParameters</span></span>
<span data-ttu-id="26558-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26558-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26558-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26558-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26558-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="26558-128">INPUTS</span></span>

### <span data-ttu-id="26558-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="26558-129">None</span></span>

## <span data-ttu-id="26558-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26558-130">OUTPUTS</span></span>

### <span data-ttu-id="26558-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26558-131">System.Boolean</span></span>

## <span data-ttu-id="26558-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="26558-132">NOTES</span></span>

## <span data-ttu-id="26558-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26558-133">RELATED LINKS</span></span>
