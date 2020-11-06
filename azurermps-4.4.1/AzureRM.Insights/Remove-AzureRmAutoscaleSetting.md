---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520081"
---
# <span data-ttu-id="7b2dc-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7b2dc-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="7b2dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2dc-103">Rimuove un'impostazione di scala.</span><span class="sxs-lookup"><span data-stu-id="7b2dc-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b2dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b2dc-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b2dc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b2dc-105">DESCRIPTION</span></span>
<span data-ttu-id="7b2dc-106">Il cmdlet **Remove-AzureRmAutoscaleSetting** rimuove un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="7b2dc-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="7b2dc-107">Devi specificare il nome dell'impostazione e il nome del gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="7b2dc-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="7b2dc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b2dc-108">EXAMPLES</span></span>

## <span data-ttu-id="7b2dc-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b2dc-109">PARAMETERS</span></span>

### <span data-ttu-id="7b2dc-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b2dc-110">-Name</span></span>
<span data-ttu-id="7b2dc-111">Specifica il nome dell'impostazione di scalabilità verticale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7b2dc-111">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="7b2dc-112">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b2dc-112">-ResourceGroup</span></span>
<span data-ttu-id="7b2dc-113">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7b2dc-113">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7b2dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2dc-114">-DefaultProfile</span></span>
<span data-ttu-id="7b2dc-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b2dc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b2dc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2dc-116">CommonParameters</span></span>
<span data-ttu-id="7b2dc-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b2dc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2dc-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b2dc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2dc-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b2dc-119">INPUTS</span></span>

## <span data-ttu-id="7b2dc-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b2dc-120">OUTPUTS</span></span>

### <span data-ttu-id="7b2dc-121">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7b2dc-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="7b2dc-122">Note</span><span class="sxs-lookup"><span data-stu-id="7b2dc-122">NOTES</span></span>

## <span data-ttu-id="7b2dc-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b2dc-123">RELATED LINKS</span></span>

[<span data-ttu-id="7b2dc-124">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7b2dc-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="7b2dc-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7b2dc-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


