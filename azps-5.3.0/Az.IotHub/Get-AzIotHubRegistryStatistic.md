---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487055"
---
# <span data-ttu-id="8e37e-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="8e37e-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="8e37e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e37e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e37e-103">Ottiene il RegistryStatistics per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="8e37e-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="8e37e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e37e-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e37e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e37e-105">DESCRIPTION</span></span>
<span data-ttu-id="8e37e-106">Ottiene il RegistryStatistics per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="8e37e-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="8e37e-107">In questo articolo vengono fornite informazioni sul numero di dispositivi totali, abilitati e disabilitati in un IotHub.</span><span class="sxs-lookup"><span data-stu-id="8e37e-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="8e37e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e37e-108">EXAMPLES</span></span>

### <span data-ttu-id="8e37e-109">Esempio 1 ottenere il RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="8e37e-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8e37e-110">Ottiene il RegistryStatistics per IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8e37e-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8e37e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e37e-111">PARAMETERS</span></span>

### <span data-ttu-id="8e37e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e37e-112">-DefaultProfile</span></span>
<span data-ttu-id="8e37e-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8e37e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e37e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e37e-114">-Name</span></span>
<span data-ttu-id="8e37e-115">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="8e37e-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="8e37e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e37e-116">-ResourceGroupName</span></span>
<span data-ttu-id="8e37e-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8e37e-117">Resource Group Name</span></span>

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

### <span data-ttu-id="8e37e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e37e-118">CommonParameters</span></span>
<span data-ttu-id="8e37e-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e37e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e37e-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e37e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e37e-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e37e-121">INPUTS</span></span>

### <span data-ttu-id="8e37e-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8e37e-122">System.String</span></span>

## <span data-ttu-id="8e37e-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e37e-123">OUTPUTS</span></span>

### <span data-ttu-id="8e37e-124">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="8e37e-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="8e37e-125">Note</span><span class="sxs-lookup"><span data-stu-id="8e37e-125">NOTES</span></span>

## <span data-ttu-id="8e37e-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e37e-126">RELATED LINKS</span></span>
