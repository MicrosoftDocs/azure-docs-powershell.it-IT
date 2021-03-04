---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: f2a2daebcb77746ae087fe527245376963fade5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956157"
---
# <span data-ttu-id="f1f6e-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="f1f6e-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="f1f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f6e-103">Crea un nuovo processo di importazione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="f1f6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1f6e-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f6e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f1f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="f1f6e-106">Crea un nuovo processo di importazione dei dispositivi per IotHub.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="f1f6e-107">Tutti i dispositivi verranno importati in IotHub dal contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="f1f6e-108">Vedere l'articolo seguente che illustra come generare l'URI di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="f1f6e-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="f1f6e-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="f1f6e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1f6e-110">EXAMPLES</span></span>

### <span data-ttu-id="f1f6e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f1f6e-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="f1f6e-112">Crea una nuova richiesta di dispositivo di importazione per il dispositivo IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="f1f6e-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="f1f6e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1f6e-113">PARAMETERS</span></span>

### <span data-ttu-id="f1f6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f6e-114">-DefaultProfile</span></span>
<span data-ttu-id="f1f6e-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f1f6e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1f6e-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f1f6e-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="f1f6e-117">Uri contenitore BLOB di input per FileUpload</span><span class="sxs-lookup"><span data-stu-id="f1f6e-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="f1f6e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f1f6e-118">-Name</span></span>
<span data-ttu-id="f1f6e-119">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="f1f6e-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="f1f6e-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f1f6e-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="f1f6e-121">Uri in cui scrivere l'output.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="f1f6e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f6e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1f6e-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f1f6e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f1f6e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1f6e-124">-Confirm</span></span>
<span data-ttu-id="f1f6e-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f6e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f6e-126">-WhatIf</span></span>
<span data-ttu-id="f1f6e-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f6e-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f6e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f6e-129">CommonParameters</span></span>
<span data-ttu-id="f1f6e-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f6e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f6e-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f6e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f6e-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="f1f6e-132">INPUTS</span></span>

### <span data-ttu-id="f1f6e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f1f6e-133">System.String</span></span>

## <span data-ttu-id="f1f6e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1f6e-134">OUTPUTS</span></span>

### <span data-ttu-id="f1f6e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="f1f6e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="f1f6e-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="f1f6e-136">NOTES</span></span>

## <span data-ttu-id="f1f6e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1f6e-137">RELATED LINKS</span></span>
