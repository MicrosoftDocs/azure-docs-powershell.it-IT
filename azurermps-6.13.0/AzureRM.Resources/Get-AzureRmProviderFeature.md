---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5969a8c5d817f206d45dcbe67d438db3fba955ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513519"
---
# <span data-ttu-id="56b54-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="56b54-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="56b54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56b54-102">SYNOPSIS</span></span>
<span data-ttu-id="56b54-103">Ottiene informazioni sulle caratteristiche del provider Azure.</span><span class="sxs-lookup"><span data-stu-id="56b54-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56b54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56b54-104">SYNTAX</span></span>

### <span data-ttu-id="56b54-105">ListAvailableParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56b54-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56b54-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="56b54-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56b54-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56b54-107">DESCRIPTION</span></span>
<span data-ttu-id="56b54-108">Il cmdlet **Get-AzureRmProviderFeature** ottiene il nome della funzionalità, il nome del provider e lo stato di registrazione per le caratteristiche del provider Azure.</span><span class="sxs-lookup"><span data-stu-id="56b54-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="56b54-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56b54-109">EXAMPLES</span></span>

### <span data-ttu-id="56b54-110">Esempio 1: ottenere tutte le funzionalità disponibili</span><span class="sxs-lookup"><span data-stu-id="56b54-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="56b54-111">Questo comando consente di ottenere tutte le funzionalità disponibili.</span><span class="sxs-lookup"><span data-stu-id="56b54-111">This command gets all available features.</span></span>

### <span data-ttu-id="56b54-112">Esempio 2: ottenere informazioni su una caratteristica specifica</span><span class="sxs-lookup"><span data-stu-id="56b54-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="56b54-113">Questo comando ottiene le informazioni per la caratteristica denominata AllowPreReleaseRegions per il provider specificato.</span><span class="sxs-lookup"><span data-stu-id="56b54-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="56b54-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56b54-114">PARAMETERS</span></span>

### <span data-ttu-id="56b54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b54-115">-DefaultProfile</span></span>
<span data-ttu-id="56b54-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56b54-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56b54-117">-Caratteristica</span><span class="sxs-lookup"><span data-stu-id="56b54-117">-FeatureName</span></span>
<span data-ttu-id="56b54-118">Specifica il nome della caratteristica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="56b54-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b54-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="56b54-119">-ListAvailable</span></span>
<span data-ttu-id="56b54-120">Indica che questo cmdlet ottiene tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="56b54-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b54-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="56b54-121">-ProviderNamespace</span></span>
<span data-ttu-id="56b54-122">Specifica lo spazio dei nomi per cui questo cmdlet ottiene le caratteristiche del provider.</span><span class="sxs-lookup"><span data-stu-id="56b54-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b54-123">CommonParameters</span></span>
<span data-ttu-id="56b54-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b54-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b54-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b54-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56b54-126">INPUTS</span></span>

## <span data-ttu-id="56b54-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56b54-127">OUTPUTS</span></span>

## <span data-ttu-id="56b54-128">Note</span><span class="sxs-lookup"><span data-stu-id="56b54-128">NOTES</span></span>

## <span data-ttu-id="56b54-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56b54-129">RELATED LINKS</span></span>

[<span data-ttu-id="56b54-130">Registro-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="56b54-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


