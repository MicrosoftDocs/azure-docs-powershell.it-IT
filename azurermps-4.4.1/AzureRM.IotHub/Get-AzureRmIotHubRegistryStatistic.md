---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: 033a7be2da102274837c881337fcb8f5bca4b879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686827"
---
# <span data-ttu-id="ddc2c-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="ddc2c-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="ddc2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddc2c-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc2c-103">Ottiene il RegistryStatistics per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="ddc2c-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddc2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddc2c-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddc2c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddc2c-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc2c-106">Ottiene il RegistryStatistics per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="ddc2c-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="ddc2c-107">In questo articolo vengono fornite informazioni sul numero di dispositivi totali, abilitati e disabilitati in un IotHub.</span><span class="sxs-lookup"><span data-stu-id="ddc2c-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="ddc2c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddc2c-108">EXAMPLES</span></span>

### <span data-ttu-id="ddc2c-109">Esempio 1 ottenere il RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="ddc2c-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ddc2c-110">Ottiene il RegistryStatictics per IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ddc2c-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ddc2c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddc2c-111">PARAMETERS</span></span>

### <span data-ttu-id="ddc2c-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddc2c-112">-Name</span></span>
<span data-ttu-id="ddc2c-113">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="ddc2c-113">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc2c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc2c-114">-ResourceGroupName</span></span>
<span data-ttu-id="ddc2c-115">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ddc2c-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc2c-116">-DefaultProfile</span></span>
<span data-ttu-id="ddc2c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc2c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddc2c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc2c-118">CommonParameters</span></span>
<span data-ttu-id="ddc2c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc2c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc2c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc2c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc2c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddc2c-121">INPUTS</span></span>

### <span data-ttu-id="ddc2c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ddc2c-122">System.String</span></span>

## <span data-ttu-id="ddc2c-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddc2c-123">OUTPUTS</span></span>

### <span data-ttu-id="ddc2c-124">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ddc2c-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ddc2c-125">Note</span><span class="sxs-lookup"><span data-stu-id="ddc2c-125">NOTES</span></span>

## <span data-ttu-id="ddc2c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddc2c-126">RELATED LINKS</span></span>

