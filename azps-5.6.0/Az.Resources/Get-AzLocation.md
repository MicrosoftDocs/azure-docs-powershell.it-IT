---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 22b9d3322baa146bcd916024b15eea96b824f2eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003133"
---
# <span data-ttu-id="00123-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="00123-101">Get-AzLocation</span></span>

## <span data-ttu-id="00123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00123-102">SYNOPSIS</span></span>
<span data-ttu-id="00123-103">Recupera tutte le posizioni e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="00123-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="00123-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00123-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00123-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00123-105">DESCRIPTION</span></span>
<span data-ttu-id="00123-106">Il cmdlet **Get-AzLocation** ottiene tutte le posizioni e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="00123-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="00123-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00123-107">EXAMPLES</span></span>

### <span data-ttu-id="00123-108">Esempio 1: Ottenere tutte le posizioni e i provider di risorse supportati</span><span class="sxs-lookup"><span data-stu-id="00123-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="00123-109">Questo comando recupera tutte le posizioni e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="00123-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="00123-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00123-110">PARAMETERS</span></span>

### <span data-ttu-id="00123-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="00123-111">-ApiVersion</span></span>
<span data-ttu-id="00123-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="00123-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="00123-113">È possibile specificare una versione diversa da quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="00123-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00123-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00123-114">-DefaultProfile</span></span>
<span data-ttu-id="00123-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="00123-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00123-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="00123-116">-Pre</span></span>
<span data-ttu-id="00123-117">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="00123-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="00123-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00123-118">CommonParameters</span></span>
<span data-ttu-id="00123-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00123-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00123-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00123-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00123-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="00123-121">INPUTS</span></span>

### <span data-ttu-id="00123-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="00123-122">None</span></span>

## <span data-ttu-id="00123-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00123-123">OUTPUTS</span></span>

### <span data-ttu-id="00123-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="00123-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="00123-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="00123-125">NOTES</span></span>

## <span data-ttu-id="00123-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00123-126">RELATED LINKS</span></span>
