---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325326"
---
# <span data-ttu-id="f6bc3-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="f6bc3-101">Get-AzLocation</span></span>

## <span data-ttu-id="f6bc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bc3-103">Ottiene tutti i percorsi e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="f6bc3-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="f6bc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6bc3-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6bc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="f6bc3-106">Il cmdlet **Get-AzLocation** ottiene tutti i percorsi e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="f6bc3-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="f6bc3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6bc3-107">EXAMPLES</span></span>

### <span data-ttu-id="f6bc3-108">Esempio 1: ottenere tutti i percorsi e i provider di risorse supportati</span><span class="sxs-lookup"><span data-stu-id="f6bc3-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="f6bc3-109">Questo comando consente di ottenere tutte le posizioni e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="f6bc3-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="f6bc3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6bc3-110">PARAMETERS</span></span>

### <span data-ttu-id="f6bc3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f6bc3-111">-ApiVersion</span></span>
<span data-ttu-id="f6bc3-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6bc3-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f6bc3-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f6bc3-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f6bc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6bc3-114">-DefaultProfile</span></span>
<span data-ttu-id="f6bc3-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f6bc3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6bc3-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="f6bc3-116">-Pre</span></span>
<span data-ttu-id="f6bc3-117">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f6bc3-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f6bc3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bc3-118">CommonParameters</span></span>
<span data-ttu-id="f6bc3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6bc3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bc3-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6bc3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bc3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6bc3-121">INPUTS</span></span>

### <span data-ttu-id="f6bc3-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f6bc3-122">None</span></span>

## <span data-ttu-id="f6bc3-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6bc3-123">OUTPUTS</span></span>

### <span data-ttu-id="f6bc3-124">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="f6bc3-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="f6bc3-125">Note</span><span class="sxs-lookup"><span data-stu-id="f6bc3-125">NOTES</span></span>

## <span data-ttu-id="f6bc3-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6bc3-126">RELATED LINKS</span></span>
