---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185639"
---
# <span data-ttu-id="e9308-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="e9308-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="e9308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9308-102">SYNOPSIS</span></span>
<span data-ttu-id="e9308-103">Ottiene RegistryStatistics per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="e9308-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="e9308-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9308-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9308-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e9308-105">DESCRIPTION</span></span>
<span data-ttu-id="e9308-106">Ottiene RegistryStatistics per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="e9308-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="e9308-107">Vengono fornite informazioni sul numero totale di dispositivi abilitati e disabilitati in IotHub.</span><span class="sxs-lookup"><span data-stu-id="e9308-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="e9308-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9308-108">EXAMPLES</span></span>

### <span data-ttu-id="e9308-109">Esempio 1: Ottenere RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="e9308-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e9308-110">Recupera RegistryStatistics per i dati IotHub denominati "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e9308-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e9308-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9308-111">PARAMETERS</span></span>

### <span data-ttu-id="e9308-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9308-112">-DefaultProfile</span></span>
<span data-ttu-id="e9308-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e9308-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9308-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e9308-114">-Name</span></span>
<span data-ttu-id="e9308-115">Nome dell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e9308-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="e9308-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9308-116">-ResourceGroupName</span></span>
<span data-ttu-id="e9308-117">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e9308-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e9308-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9308-118">CommonParameters</span></span>
<span data-ttu-id="e9308-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9308-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9308-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9308-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9308-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="e9308-121">INPUTS</span></span>

### <span data-ttu-id="e9308-122">System.String</span><span class="sxs-lookup"><span data-stu-id="e9308-122">System.String</span></span>

## <span data-ttu-id="e9308-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9308-123">OUTPUTS</span></span>

### <span data-ttu-id="e9308-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="e9308-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="e9308-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="e9308-125">NOTES</span></span>

## <span data-ttu-id="e9308-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9308-126">RELATED LINKS</span></span>
