---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 3191f4e451ec010a3918130142d08da6f08b3990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521230"
---
# <span data-ttu-id="1e3eb-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="1e3eb-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="1e3eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3eb-103">Crea un nuovo processo per i dispositivi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e3eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e3eb-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e3eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e3eb-105">DESCRIPTION</span></span>
<span data-ttu-id="1e3eb-106">Crea un nuovo processo per i dispositivi di esportazione per IotHub.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="1e3eb-107">In questo modo verranno esportati tutti i dispositivi nel contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="1e3eb-108">Vedere l'articolo seguente su come generare l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="1e3eb-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="1e3eb-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="1e3eb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e3eb-110">EXAMPLES</span></span>

### <span data-ttu-id="1e3eb-111">Esempio 1 emettere una richiesta di dispositivo di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="1e3eb-112">Crea una nuova richiesta di dispositivo di esportazione per il IotHub "myiothub" escluse le chiavi.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="1e3eb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e3eb-113">PARAMETERS</span></span>

### <span data-ttu-id="1e3eb-114">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="1e3eb-114">-ExportBlobContainerUri</span></span>
<span data-ttu-id="1e3eb-115">L'URI a cui esportare il BLOB.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-115">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="1e3eb-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e3eb-116">-Name</span></span>
<span data-ttu-id="1e3eb-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="1e3eb-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="1e3eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3eb-118">-ResourceGroupName</span></span>
<span data-ttu-id="1e3eb-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1e3eb-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1e3eb-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e3eb-120">-Confirm</span></span>
<span data-ttu-id="1e3eb-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e3eb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3eb-122">-WhatIf</span></span>
<span data-ttu-id="1e3eb-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e3eb-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e3eb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3eb-125">-DefaultProfile</span></span>
<span data-ttu-id="1e3eb-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e3eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3eb-127">CommonParameters</span></span>
<span data-ttu-id="1e3eb-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e3eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3eb-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e3eb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3eb-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e3eb-130">INPUTS</span></span>

### <span data-ttu-id="1e3eb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3eb-131">System.String</span></span>

## <span data-ttu-id="1e3eb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e3eb-132">OUTPUTS</span></span>

### <span data-ttu-id="1e3eb-133">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="1e3eb-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="1e3eb-134">Note</span><span class="sxs-lookup"><span data-stu-id="1e3eb-134">NOTES</span></span>

## <span data-ttu-id="1e3eb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e3eb-135">RELATED LINKS</span></span>

