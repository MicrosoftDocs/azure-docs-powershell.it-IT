---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 93c51e71cf912a072daafd721d9e9626ccefbb06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866333"
---
# <span data-ttu-id="ab21a-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ab21a-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="ab21a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab21a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab21a-103">Rimuove un'impostazione di scala.</span><span class="sxs-lookup"><span data-stu-id="ab21a-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab21a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab21a-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab21a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab21a-105">DESCRIPTION</span></span>
<span data-ttu-id="ab21a-106">Il cmdlet **Remove-AzureRmAutoscaleSetting** rimuove un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="ab21a-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="ab21a-107">Devi specificare il nome dell'impostazione e il nome del gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="ab21a-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="ab21a-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ab21a-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ab21a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab21a-109">EXAMPLES</span></span>

## <span data-ttu-id="ab21a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab21a-110">PARAMETERS</span></span>

### <span data-ttu-id="ab21a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab21a-111">-DefaultProfile</span></span>
<span data-ttu-id="ab21a-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab21a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab21a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab21a-113">-Name</span></span>
<span data-ttu-id="ab21a-114">Specifica il nome dell'impostazione di scalabilità verticale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ab21a-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab21a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab21a-115">-ResourceGroupName</span></span>
<span data-ttu-id="ab21a-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab21a-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab21a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab21a-117">-Confirm</span></span>
<span data-ttu-id="ab21a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab21a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab21a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab21a-119">-WhatIf</span></span>
<span data-ttu-id="ab21a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab21a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab21a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab21a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab21a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab21a-122">CommonParameters</span></span>
<span data-ttu-id="ab21a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab21a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab21a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab21a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab21a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab21a-125">INPUTS</span></span>

### <span data-ttu-id="ab21a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ab21a-126">System.String</span></span>

## <span data-ttu-id="ab21a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab21a-127">OUTPUTS</span></span>

### <span data-ttu-id="ab21a-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ab21a-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ab21a-129">Note</span><span class="sxs-lookup"><span data-stu-id="ab21a-129">NOTES</span></span>

## <span data-ttu-id="ab21a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab21a-130">RELATED LINKS</span></span>

[<span data-ttu-id="ab21a-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ab21a-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="ab21a-132">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ab21a-132">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


