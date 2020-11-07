---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: 684b892d2c2cc995e12ae6327541f13428da270f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687858"
---
# <span data-ttu-id="c391d-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="c391d-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="c391d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c391d-102">SYNOPSIS</span></span>
<span data-ttu-id="c391d-103">Ottiene le informazioni su un processo di IotHub.</span><span class="sxs-lookup"><span data-stu-id="c391d-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c391d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c391d-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c391d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c391d-105">DESCRIPTION</span></span>
<span data-ttu-id="c391d-106">Ottiene le informazioni su un processo di IotHub.</span><span class="sxs-lookup"><span data-stu-id="c391d-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="c391d-107">Un processo di IotHub viene creato quando un'operazione di importazione o esportazione viene initialted usando i comandi New-AzureRmIotHubExportDevices o New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="c391d-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="c391d-108">È possibile elencare tutti i processi o filtrare i processi in base all'identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="c391d-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="c391d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c391d-109">EXAMPLES</span></span>

### <span data-ttu-id="c391d-110">Esempio 1 elenca tutti i processi</span><span class="sxs-lookup"><span data-stu-id="c391d-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c391d-111">Ottiene tutti i processi per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c391d-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="c391d-112">Esempio 2 ottenere un processo specifico</span><span class="sxs-lookup"><span data-stu-id="c391d-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="c391d-113">Ottiene le informazioni sul processo con l'identificatore "3630fc31-4caa-43e8-A232-ea0577221cb2" per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c391d-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c391d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c391d-114">PARAMETERS</span></span>

### <span data-ttu-id="c391d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c391d-115">-DefaultProfile</span></span>
<span data-ttu-id="c391d-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c391d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c391d-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="c391d-117">-JobId</span></span>
<span data-ttu-id="c391d-118">Identificatore processo.</span><span class="sxs-lookup"><span data-stu-id="c391d-118">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c391d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c391d-119">-Name</span></span>
<span data-ttu-id="c391d-120">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="c391d-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="c391d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c391d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c391d-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c391d-122">Resource Group Name</span></span>

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

### <span data-ttu-id="c391d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c391d-123">CommonParameters</span></span>
<span data-ttu-id="c391d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c391d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c391d-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c391d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c391d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c391d-126">INPUTS</span></span>

### <span data-ttu-id="c391d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c391d-127">System.String</span></span>

## <span data-ttu-id="c391d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c391d-128">OUTPUTS</span></span>

### <span data-ttu-id="c391d-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="c391d-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="c391d-130">Note</span><span class="sxs-lookup"><span data-stu-id="c391d-130">NOTES</span></span>

## <span data-ttu-id="c391d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c391d-131">RELATED LINKS</span></span>
