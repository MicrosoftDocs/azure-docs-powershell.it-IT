---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191320"
---
# <span data-ttu-id="1a40e-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="1a40e-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="1a40e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a40e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a40e-103">Ottiene le informazioni su un processo di IotHub.</span><span class="sxs-lookup"><span data-stu-id="1a40e-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="1a40e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a40e-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a40e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a40e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a40e-106">Ottiene le informazioni su un processo di IotHub.</span><span class="sxs-lookup"><span data-stu-id="1a40e-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="1a40e-107">Viene creato un processo IotHub quando un'operazione di importazione o esportazione viene inizializzata con i comandi New-AzIotHubExportDevices o New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="1a40e-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="1a40e-108">È possibile elencare tutti i processi o filtrare i processi in base all'identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="1a40e-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="1a40e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a40e-109">EXAMPLES</span></span>

### <span data-ttu-id="1a40e-110">Esempio 1 elenca tutti i processi</span><span class="sxs-lookup"><span data-stu-id="1a40e-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1a40e-111">Ottiene tutti i processi per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1a40e-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="1a40e-112">Esempio 2 ottenere un processo specifico</span><span class="sxs-lookup"><span data-stu-id="1a40e-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="1a40e-113">Ottiene le informazioni sul processo con l'identificatore "3630fc31-4caa-43e8-A232-ea0577221cb2" per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1a40e-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="1a40e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a40e-114">PARAMETERS</span></span>

### <span data-ttu-id="1a40e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a40e-115">-DefaultProfile</span></span>
<span data-ttu-id="1a40e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1a40e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a40e-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="1a40e-117">-JobId</span></span>
<span data-ttu-id="1a40e-118">Identificatore processo.</span><span class="sxs-lookup"><span data-stu-id="1a40e-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="1a40e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a40e-119">-Name</span></span>
<span data-ttu-id="1a40e-120">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="1a40e-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="1a40e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a40e-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a40e-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1a40e-122">Resource Group Name</span></span>

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

### <span data-ttu-id="1a40e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a40e-123">CommonParameters</span></span>
<span data-ttu-id="1a40e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a40e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a40e-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a40e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a40e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a40e-126">INPUTS</span></span>

### <span data-ttu-id="1a40e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1a40e-127">System.String</span></span>

## <span data-ttu-id="1a40e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a40e-128">OUTPUTS</span></span>

### <span data-ttu-id="1a40e-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="1a40e-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="1a40e-130">Note</span><span class="sxs-lookup"><span data-stu-id="1a40e-130">NOTES</span></span>

## <span data-ttu-id="1a40e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a40e-131">RELATED LINKS</span></span>