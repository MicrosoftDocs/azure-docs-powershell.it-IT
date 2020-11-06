---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507440"
---
# <span data-ttu-id="05ff4-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="05ff4-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="05ff4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="05ff4-103">Rimuovere il contenuto nello sportello anteriore</span><span class="sxs-lookup"><span data-stu-id="05ff4-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05ff4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05ff4-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ff4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="05ff4-106">Remove-AzureRmFrontDoorContent Elimina il contenuto memorizzato nella cache in uno sportello anteriore</span><span class="sxs-lookup"><span data-stu-id="05ff4-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="05ff4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="05ff4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05ff4-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="05ff4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05ff4-109">PARAMETERS</span></span>

### <span data-ttu-id="05ff4-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="05ff4-110">-ContentPath</span></span>
<span data-ttu-id="05ff4-111">Percorsi per il contenuto da eliminare.</span><span class="sxs-lookup"><span data-stu-id="05ff4-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="05ff4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ff4-112">-DefaultProfile</span></span>
<span data-ttu-id="05ff4-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05ff4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05ff4-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="05ff4-114">-Name</span></span>
<span data-ttu-id="05ff4-115">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="05ff4-115">Front Door name.</span></span>

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

### <span data-ttu-id="05ff4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05ff4-116">-PassThru</span></span>
<span data-ttu-id="05ff4-117">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="05ff4-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="05ff4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ff4-118">-ResourceGroupName</span></span>
<span data-ttu-id="05ff4-119">Nome del gruppo di risorse dello sportello anteriore</span><span class="sxs-lookup"><span data-stu-id="05ff4-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="05ff4-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05ff4-120">-Confirm</span></span>
<span data-ttu-id="05ff4-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ff4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ff4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ff4-122">-WhatIf</span></span>
<span data-ttu-id="05ff4-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05ff4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ff4-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05ff4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ff4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ff4-125">CommonParameters</span></span>
<span data-ttu-id="05ff4-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ff4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ff4-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ff4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ff4-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05ff4-128">INPUTS</span></span>

### <span data-ttu-id="05ff4-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="05ff4-129">None</span></span>

## <span data-ttu-id="05ff4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05ff4-130">OUTPUTS</span></span>

### <span data-ttu-id="05ff4-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05ff4-131">System.Boolean</span></span>

## <span data-ttu-id="05ff4-132">Note</span><span class="sxs-lookup"><span data-stu-id="05ff4-132">NOTES</span></span>

## <span data-ttu-id="05ff4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05ff4-133">RELATED LINKS</span></span>
