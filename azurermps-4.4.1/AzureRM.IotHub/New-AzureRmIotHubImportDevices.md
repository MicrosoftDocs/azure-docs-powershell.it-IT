---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: f8c2d2b7508e07dd5f42287a95623c3a6cf245de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521228"
---
# <span data-ttu-id="b1934-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="b1934-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="b1934-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1934-102">SYNOPSIS</span></span>
<span data-ttu-id="b1934-103">Crea un nuovo processo di importazione di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b1934-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1934-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1934-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1934-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1934-105">DESCRIPTION</span></span>
<span data-ttu-id="b1934-106">Crea un nuovo processo di importazione di dispositivi per IotHub.</span><span class="sxs-lookup"><span data-stu-id="b1934-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="b1934-107">In questo modo verranno importati tutti i dispositivi in IotHub dal contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="b1934-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="b1934-108">Vedere l'articolo seguente su come generare l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="b1934-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="b1934-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="b1934-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="b1934-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1934-110">EXAMPLES</span></span>

### <span data-ttu-id="b1934-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1934-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="b1934-112">Crea una nuova richiesta di importazione di dispositivi per il IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="b1934-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="b1934-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1934-113">PARAMETERS</span></span>

### <span data-ttu-id="b1934-114">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="b1934-114">-InputBlobContainerUri</span></span>
<span data-ttu-id="b1934-115">URI contenitore BLOB di input per FileUpload</span><span class="sxs-lookup"><span data-stu-id="b1934-115">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1934-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1934-116">-Name</span></span>
<span data-ttu-id="b1934-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="b1934-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="b1934-118">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="b1934-118">-OutputBlobContainerUri</span></span>
<span data-ttu-id="b1934-119">L'URI a cui scrivere l'output.</span><span class="sxs-lookup"><span data-stu-id="b1934-119">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1934-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1934-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1934-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b1934-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b1934-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1934-122">-Confirm</span></span>
<span data-ttu-id="b1934-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1934-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1934-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1934-124">-WhatIf</span></span>
<span data-ttu-id="b1934-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1934-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1934-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1934-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1934-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1934-127">-DefaultProfile</span></span>
<span data-ttu-id="b1934-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1934-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1934-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1934-129">CommonParameters</span></span>
<span data-ttu-id="b1934-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1934-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1934-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1934-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1934-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1934-132">INPUTS</span></span>

### <span data-ttu-id="b1934-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b1934-133">System.String</span></span>

## <span data-ttu-id="b1934-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1934-134">OUTPUTS</span></span>

### <span data-ttu-id="b1934-135">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="b1934-135">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="b1934-136">Note</span><span class="sxs-lookup"><span data-stu-id="b1934-136">NOTES</span></span>

## <span data-ttu-id="b1934-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1934-137">RELATED LINKS</span></span>

