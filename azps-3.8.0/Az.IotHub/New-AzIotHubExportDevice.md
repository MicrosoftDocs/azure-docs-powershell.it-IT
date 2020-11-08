---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 3b04e0598897fb206ca781f4f19d9e8e2ec206dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021775"
---
# <span data-ttu-id="1326a-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="1326a-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="1326a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1326a-102">SYNOPSIS</span></span>
<span data-ttu-id="1326a-103">Crea un nuovo processo per i dispositivi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1326a-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="1326a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1326a-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1326a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1326a-105">DESCRIPTION</span></span>
<span data-ttu-id="1326a-106">Crea un nuovo processo per i dispositivi di esportazione per IotHub.</span><span class="sxs-lookup"><span data-stu-id="1326a-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="1326a-107">In questo modo verranno esportati tutti i dispositivi nel contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="1326a-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="1326a-108">Vedere l'articolo seguente su come generare l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="1326a-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="1326a-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="1326a-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="1326a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1326a-110">EXAMPLES</span></span>

### <span data-ttu-id="1326a-111">Esempio 1 emettere una richiesta di dispositivo di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1326a-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="1326a-112">Crea una nuova richiesta di dispositivo di esportazione per il IotHub "myiothub" escluse le chiavi.</span><span class="sxs-lookup"><span data-stu-id="1326a-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="1326a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1326a-113">PARAMETERS</span></span>

### <span data-ttu-id="1326a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1326a-114">-DefaultProfile</span></span>
<span data-ttu-id="1326a-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1326a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1326a-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="1326a-116">-ExcludeKeys</span></span>
<span data-ttu-id="1326a-117">Consente di esportare dispositivi senza tasti.</span><span class="sxs-lookup"><span data-stu-id="1326a-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="1326a-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="1326a-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="1326a-119">L'URI a cui esportare il BLOB.</span><span class="sxs-lookup"><span data-stu-id="1326a-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="1326a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1326a-120">-Name</span></span>
<span data-ttu-id="1326a-121">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="1326a-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="1326a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1326a-122">-ResourceGroupName</span></span>
<span data-ttu-id="1326a-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1326a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1326a-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1326a-124">-Confirm</span></span>
<span data-ttu-id="1326a-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1326a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1326a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1326a-126">-WhatIf</span></span>
<span data-ttu-id="1326a-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1326a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1326a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1326a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1326a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1326a-129">CommonParameters</span></span>
<span data-ttu-id="1326a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1326a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1326a-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1326a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1326a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1326a-132">INPUTS</span></span>

### <span data-ttu-id="1326a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1326a-133">System.String</span></span>

## <span data-ttu-id="1326a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1326a-134">OUTPUTS</span></span>

### <span data-ttu-id="1326a-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="1326a-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="1326a-136">Note</span><span class="sxs-lookup"><span data-stu-id="1326a-136">NOTES</span></span>

## <span data-ttu-id="1326a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1326a-137">RELATED LINKS</span></span>
