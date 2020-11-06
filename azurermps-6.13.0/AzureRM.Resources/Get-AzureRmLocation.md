---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 6052a621b43cd0b51170e9a502a38df46d38e17d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514860"
---
# <span data-ttu-id="61956-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="61956-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="61956-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61956-102">SYNOPSIS</span></span>
<span data-ttu-id="61956-103">Ottiene tutti i percorsi e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="61956-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61956-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61956-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61956-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61956-105">DESCRIPTION</span></span>
<span data-ttu-id="61956-106">Il cmdlet **Get-AzureRmLocation** ottiene tutti i percorsi e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="61956-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="61956-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61956-107">EXAMPLES</span></span>

### <span data-ttu-id="61956-108">Esempio 1: ottenere tutti i percorsi e i provider di risorse supportati</span><span class="sxs-lookup"><span data-stu-id="61956-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="61956-109">Questo comando consente di ottenere tutte le posizioni e i provider di risorse supportati per ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="61956-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="61956-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61956-110">PARAMETERS</span></span>

### <span data-ttu-id="61956-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="61956-111">-ApiVersion</span></span>
<span data-ttu-id="61956-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="61956-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="61956-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="61956-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="61956-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61956-114">-DefaultProfile</span></span>
<span data-ttu-id="61956-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="61956-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61956-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="61956-116">-Pre</span></span>
<span data-ttu-id="61956-117">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="61956-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="61956-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61956-118">CommonParameters</span></span>
<span data-ttu-id="61956-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61956-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61956-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61956-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61956-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61956-121">INPUTS</span></span>

## <span data-ttu-id="61956-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61956-122">OUTPUTS</span></span>

## <span data-ttu-id="61956-123">Note</span><span class="sxs-lookup"><span data-stu-id="61956-123">NOTES</span></span>

## <span data-ttu-id="61956-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61956-124">RELATED LINKS</span></span>
