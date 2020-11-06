---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512603"
---
# <span data-ttu-id="32849-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="32849-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="32849-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32849-102">SYNOPSIS</span></span>
<span data-ttu-id="32849-103">Rimuove un'impostazione di scala.</span><span class="sxs-lookup"><span data-stu-id="32849-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32849-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32849-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32849-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32849-105">DESCRIPTION</span></span>
<span data-ttu-id="32849-106">Il cmdlet **Remove-AzureRmAutoscaleSetting** rimuove un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="32849-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="32849-107">Devi specificare il nome dell'impostazione e il nome del gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="32849-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="32849-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="32849-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="32849-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32849-109">EXAMPLES</span></span>

## <span data-ttu-id="32849-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32849-110">PARAMETERS</span></span>

### <span data-ttu-id="32849-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32849-111">-DefaultProfile</span></span>
<span data-ttu-id="32849-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="32849-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32849-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="32849-113">-Name</span></span>
<span data-ttu-id="32849-114">Specifica il nome dell'impostazione di scalabilità verticale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="32849-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32849-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32849-115">-ResourceGroupName</span></span>
<span data-ttu-id="32849-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32849-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32849-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32849-117">CommonParameters</span></span>
<span data-ttu-id="32849-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32849-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32849-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32849-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32849-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32849-120">INPUTS</span></span>

### <span data-ttu-id="32849-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="32849-121">None</span></span>
<span data-ttu-id="32849-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="32849-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32849-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32849-123">OUTPUTS</span></span>

### <span data-ttu-id="32849-124">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="32849-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="32849-125">Note</span><span class="sxs-lookup"><span data-stu-id="32849-125">NOTES</span></span>

## <span data-ttu-id="32849-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32849-126">RELATED LINKS</span></span>

[<span data-ttu-id="32849-127">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="32849-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="32849-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="32849-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


