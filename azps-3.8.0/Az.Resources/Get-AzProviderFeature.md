---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020578"
---
# <span data-ttu-id="79493-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="79493-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="79493-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79493-102">SYNOPSIS</span></span>
<span data-ttu-id="79493-103">Ottiene informazioni sulle caratteristiche del provider Azure.</span><span class="sxs-lookup"><span data-stu-id="79493-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="79493-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79493-104">SYNTAX</span></span>

### <span data-ttu-id="79493-105">ListAvailableParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79493-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79493-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="79493-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79493-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79493-107">DESCRIPTION</span></span>
<span data-ttu-id="79493-108">Il cmdlet **Get-AzProviderFeature** ottiene il nome della funzionalità, il nome del provider e lo stato di registrazione per le caratteristiche del provider Azure.</span><span class="sxs-lookup"><span data-stu-id="79493-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="79493-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79493-109">EXAMPLES</span></span>

### <span data-ttu-id="79493-110">Esempio 1: ottenere tutte le funzionalità disponibili</span><span class="sxs-lookup"><span data-stu-id="79493-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="79493-111">Questo comando consente di ottenere tutte le funzionalità disponibili.</span><span class="sxs-lookup"><span data-stu-id="79493-111">This command gets all available features.</span></span>

### <span data-ttu-id="79493-112">Esempio 2: ottenere informazioni su una caratteristica specifica</span><span class="sxs-lookup"><span data-stu-id="79493-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="79493-113">Questo comando ottiene le informazioni per la caratteristica denominata AllowPreReleaseRegions per il provider specificato.</span><span class="sxs-lookup"><span data-stu-id="79493-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="79493-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79493-114">PARAMETERS</span></span>

### <span data-ttu-id="79493-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79493-115">-DefaultProfile</span></span>
<span data-ttu-id="79493-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79493-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79493-117">-Caratteristica</span><span class="sxs-lookup"><span data-stu-id="79493-117">-FeatureName</span></span>
<span data-ttu-id="79493-118">Specifica il nome della caratteristica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="79493-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="79493-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="79493-119">-ListAvailable</span></span>
<span data-ttu-id="79493-120">Indica che questo cmdlet ottiene tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="79493-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="79493-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="79493-121">-ProviderNamespace</span></span>
<span data-ttu-id="79493-122">Specifica lo spazio dei nomi per cui questo cmdlet ottiene le caratteristiche del provider.</span><span class="sxs-lookup"><span data-stu-id="79493-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="79493-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79493-123">CommonParameters</span></span>
<span data-ttu-id="79493-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79493-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79493-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79493-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79493-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79493-126">INPUTS</span></span>

### <span data-ttu-id="79493-127">System. String</span><span class="sxs-lookup"><span data-stu-id="79493-127">System.String</span></span>

## <span data-ttu-id="79493-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79493-128">OUTPUTS</span></span>

### <span data-ttu-id="79493-129">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="79493-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="79493-130">Note</span><span class="sxs-lookup"><span data-stu-id="79493-130">NOTES</span></span>

## <span data-ttu-id="79493-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79493-131">RELATED LINKS</span></span>

[<span data-ttu-id="79493-132">Registro-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="79493-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


