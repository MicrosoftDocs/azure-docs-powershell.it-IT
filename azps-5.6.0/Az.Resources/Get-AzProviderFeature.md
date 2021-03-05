---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 67a0eee0dfe46b7b846958e1aa3f2be515a6b213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016046"
---
# <span data-ttu-id="607f3-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="607f3-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="607f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="607f3-102">SYNOPSIS</span></span>
<span data-ttu-id="607f3-103">Recupera informazioni sulle funzionalità del provider di Azure.</span><span class="sxs-lookup"><span data-stu-id="607f3-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="607f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="607f3-104">SYNTAX</span></span>

### <span data-ttu-id="607f3-105">ListAvailableParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="607f3-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="607f3-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="607f3-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="607f3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="607f3-107">DESCRIPTION</span></span>
<span data-ttu-id="607f3-108">Il cmdlet **Get-AzProviderFeature** ottiene il nome della caratteristica, il nome del provider e lo stato di registrazione per le caratteristiche del provider di Azure.</span><span class="sxs-lookup"><span data-stu-id="607f3-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="607f3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="607f3-109">EXAMPLES</span></span>

### <span data-ttu-id="607f3-110">Esempio 1: Ottenere tutte le funzionalità disponibili</span><span class="sxs-lookup"><span data-stu-id="607f3-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="607f3-111">Questo comando recupera tutte le funzionalità disponibili.</span><span class="sxs-lookup"><span data-stu-id="607f3-111">This command gets all available features.</span></span>

### <span data-ttu-id="607f3-112">Esempio 2: Ottenere informazioni su una caratteristica specifica</span><span class="sxs-lookup"><span data-stu-id="607f3-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="607f3-113">Questo comando recupera informazioni per la caratteristica denominata AllowPreReleaseRegions per il provider specificato.</span><span class="sxs-lookup"><span data-stu-id="607f3-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="607f3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="607f3-114">PARAMETERS</span></span>

### <span data-ttu-id="607f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607f3-115">-DefaultProfile</span></span>
<span data-ttu-id="607f3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="607f3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="607f3-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="607f3-117">-FeatureName</span></span>
<span data-ttu-id="607f3-118">Specifica il nome della funzionalità da ottenere.</span><span class="sxs-lookup"><span data-stu-id="607f3-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="607f3-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="607f3-119">-ListAvailable</span></span>
<span data-ttu-id="607f3-120">Indica che questo cmdlet ottiene tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="607f3-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="607f3-121">-Provider Provider</span><span class="sxs-lookup"><span data-stu-id="607f3-121">-ProviderNamespace</span></span>
<span data-ttu-id="607f3-122">Specifica lo spazio dei nomi per cui questo cmdlet ottiene le caratteristiche del provider.</span><span class="sxs-lookup"><span data-stu-id="607f3-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="607f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607f3-123">CommonParameters</span></span>
<span data-ttu-id="607f3-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="607f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607f3-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="607f3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607f3-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="607f3-126">INPUTS</span></span>

### <span data-ttu-id="607f3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="607f3-127">System.String</span></span>

## <span data-ttu-id="607f3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="607f3-128">OUTPUTS</span></span>

### <span data-ttu-id="607f3-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="607f3-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="607f3-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="607f3-130">NOTES</span></span>

## <span data-ttu-id="607f3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="607f3-131">RELATED LINKS</span></span>

[<span data-ttu-id="607f3-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="607f3-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


