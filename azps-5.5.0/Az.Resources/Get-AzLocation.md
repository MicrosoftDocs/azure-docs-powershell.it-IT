---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178830"
---
# <span data-ttu-id="3cc26-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="3cc26-101">Get-AzLocation</span></span>

## <span data-ttu-id="3cc26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc26-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc26-103">Ottiene tutte le posizioni e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="3cc26-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="3cc26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cc26-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cc26-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3cc26-105">DESCRIPTION</span></span>
<span data-ttu-id="3cc26-106">Il cmdlet **Get-AzLocation** ottiene tutte le posizioni e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="3cc26-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="3cc26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cc26-107">EXAMPLES</span></span>

### <span data-ttu-id="3cc26-108">Esempio 1: Ottenere tutte le posizioni e i provider di risorse supportati</span><span class="sxs-lookup"><span data-stu-id="3cc26-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="3cc26-109">Questo comando recupera tutte le posizioni e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="3cc26-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="3cc26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cc26-110">PARAMETERS</span></span>

### <span data-ttu-id="3cc26-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3cc26-111">-ApiVersion</span></span>
<span data-ttu-id="3cc26-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="3cc26-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3cc26-113">È possibile specificare una versione diversa da quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="3cc26-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3cc26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc26-114">-DefaultProfile</span></span>
<span data-ttu-id="3cc26-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3cc26-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cc26-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="3cc26-116">-Pre</span></span>
<span data-ttu-id="3cc26-117">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="3cc26-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3cc26-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc26-118">CommonParameters</span></span>
<span data-ttu-id="3cc26-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc26-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc26-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cc26-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc26-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="3cc26-121">INPUTS</span></span>

### <span data-ttu-id="3cc26-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3cc26-122">None</span></span>

## <span data-ttu-id="3cc26-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cc26-123">OUTPUTS</span></span>

### <span data-ttu-id="3cc26-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="3cc26-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="3cc26-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="3cc26-125">NOTES</span></span>

## <span data-ttu-id="3cc26-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cc26-126">RELATED LINKS</span></span>
