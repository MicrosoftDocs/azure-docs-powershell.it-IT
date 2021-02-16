---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185695"
---
# <span data-ttu-id="91403-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="91403-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="91403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91403-102">SYNOPSIS</span></span>
<span data-ttu-id="91403-103">Ottiene le informazioni su un processo di IotHub.</span><span class="sxs-lookup"><span data-stu-id="91403-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="91403-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91403-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91403-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="91403-105">DESCRIPTION</span></span>
<span data-ttu-id="91403-106">Ottiene le informazioni su un processo di IotHub.</span><span class="sxs-lookup"><span data-stu-id="91403-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="91403-107">Viene creato un processo IotHub quando viene inizializzata un'operazione di importazione o esportazione usando i comandi New-AzIotHubExportDevices o New-AzIotHubImportDevices importazione.</span><span class="sxs-lookup"><span data-stu-id="91403-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="91403-108">È possibile elencare tutti i processi o filtrare i processi in base all'identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="91403-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="91403-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91403-109">EXAMPLES</span></span>

### <span data-ttu-id="91403-110">Esempio 1: elencare tutti i processi</span><span class="sxs-lookup"><span data-stu-id="91403-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="91403-111">Recupera tutti i processi per il sito IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="91403-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="91403-112">Esempio 2: Ottenere un processo specifico</span><span class="sxs-lookup"><span data-stu-id="91403-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="91403-113">Ottiene informazioni sul processo con l'identificatore "3630fc31-4caa-43e8-a232-ea0577221cb2" per il sito IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="91403-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="91403-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91403-114">PARAMETERS</span></span>

### <span data-ttu-id="91403-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91403-115">-DefaultProfile</span></span>
<span data-ttu-id="91403-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="91403-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91403-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="91403-117">-JobId</span></span>
<span data-ttu-id="91403-118">L'identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="91403-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="91403-119">-Name</span><span class="sxs-lookup"><span data-stu-id="91403-119">-Name</span></span>
<span data-ttu-id="91403-120">Nome dell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="91403-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="91403-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91403-121">-ResourceGroupName</span></span>
<span data-ttu-id="91403-122">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="91403-122">Resource Group Name</span></span>

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

### <span data-ttu-id="91403-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91403-123">CommonParameters</span></span>
<span data-ttu-id="91403-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91403-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91403-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91403-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91403-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="91403-126">INPUTS</span></span>

### <span data-ttu-id="91403-127">System.String</span><span class="sxs-lookup"><span data-stu-id="91403-127">System.String</span></span>

## <span data-ttu-id="91403-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91403-128">OUTPUTS</span></span>

### <span data-ttu-id="91403-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="91403-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="91403-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="91403-130">NOTES</span></span>

## <span data-ttu-id="91403-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91403-131">RELATED LINKS</span></span>
