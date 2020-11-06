---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519549"
---
# <span data-ttu-id="808a4-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="808a4-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="808a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="808a4-102">SYNOPSIS</span></span>
<span data-ttu-id="808a4-103">Ottiene informazioni sulle caratteristiche del provider Azure.</span><span class="sxs-lookup"><span data-stu-id="808a4-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="808a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="808a4-104">SYNTAX</span></span>

### <span data-ttu-id="808a4-105">ListAvailableParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="808a4-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808a4-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="808a4-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="808a4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="808a4-107">DESCRIPTION</span></span>
<span data-ttu-id="808a4-108">Il cmdlet **Get-AzureRmProviderFeature** ottiene il nome della funzionalità, il nome del provider e lo stato di registrazione per le caratteristiche del provider Azure.</span><span class="sxs-lookup"><span data-stu-id="808a4-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="808a4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="808a4-109">EXAMPLES</span></span>

### <span data-ttu-id="808a4-110">Esempio 1: ottenere tutte le funzionalità disponibili</span><span class="sxs-lookup"><span data-stu-id="808a4-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="808a4-111">Questo comando consente di ottenere tutte le funzionalità disponibili.</span><span class="sxs-lookup"><span data-stu-id="808a4-111">This command gets all available features.</span></span>

### <span data-ttu-id="808a4-112">Esempio 2: ottenere informazioni su una caratteristica specifica</span><span class="sxs-lookup"><span data-stu-id="808a4-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="808a4-113">Questo comando ottiene le informazioni per la caratteristica denominata AllowPreReleaseRegions per il provider specificato.</span><span class="sxs-lookup"><span data-stu-id="808a4-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="808a4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="808a4-114">PARAMETERS</span></span>

### <span data-ttu-id="808a4-115">-Caratteristica</span><span class="sxs-lookup"><span data-stu-id="808a4-115">-FeatureName</span></span>
<span data-ttu-id="808a4-116">Specifica il nome della caratteristica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="808a4-116">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="808a4-117">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="808a4-117">-ListAvailable</span></span>
<span data-ttu-id="808a4-118">Indica che questo cmdlet ottiene tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="808a4-118">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="808a4-119">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="808a4-119">-ProviderNamespace</span></span>
<span data-ttu-id="808a4-120">Specifica lo spazio dei nomi per cui questo cmdlet ottiene le caratteristiche del provider.</span><span class="sxs-lookup"><span data-stu-id="808a4-120">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="808a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808a4-121">-DefaultProfile</span></span>
<span data-ttu-id="808a4-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="808a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="808a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808a4-123">CommonParameters</span></span>
<span data-ttu-id="808a4-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808a4-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808a4-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="808a4-126">INPUTS</span></span>

## <span data-ttu-id="808a4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="808a4-127">OUTPUTS</span></span>

### <span data-ttu-id="808a4-128">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="808a4-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="808a4-129">Note</span><span class="sxs-lookup"><span data-stu-id="808a4-129">NOTES</span></span>

## <span data-ttu-id="808a4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="808a4-130">RELATED LINKS</span></span>

[<span data-ttu-id="808a4-131">Registro-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="808a4-131">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


