---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: 50f0652f477edad13fb661683b1ee2f2f13fef9d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863089"
---
# <span data-ttu-id="a626a-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="a626a-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="a626a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a626a-102">SYNOPSIS</span></span>
<span data-ttu-id="a626a-103">Crea un nuovo processo di importazione di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a626a-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="a626a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a626a-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a626a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a626a-105">DESCRIPTION</span></span>
<span data-ttu-id="a626a-106">Crea un nuovo processo di importazione di dispositivi per IotHub.</span><span class="sxs-lookup"><span data-stu-id="a626a-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="a626a-107">In questo modo verranno importati tutti i dispositivi in IotHub dal contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="a626a-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="a626a-108">Vedere l'articolo seguente su come generare l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="a626a-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="a626a-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="a626a-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="a626a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a626a-110">EXAMPLES</span></span>

### <span data-ttu-id="a626a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a626a-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="a626a-112">Crea una nuova richiesta di importazione di dispositivi per il IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a626a-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="a626a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a626a-113">PARAMETERS</span></span>

### <span data-ttu-id="a626a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a626a-114">-DefaultProfile</span></span>
<span data-ttu-id="a626a-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a626a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a626a-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a626a-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="a626a-117">URI contenitore BLOB di input per FileUpload</span><span class="sxs-lookup"><span data-stu-id="a626a-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="a626a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a626a-118">-Name</span></span>
<span data-ttu-id="a626a-119">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="a626a-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="a626a-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a626a-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="a626a-121">L'URI a cui scrivere l'output.</span><span class="sxs-lookup"><span data-stu-id="a626a-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="a626a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a626a-122">-ResourceGroupName</span></span>
<span data-ttu-id="a626a-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a626a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a626a-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a626a-124">-Confirm</span></span>
<span data-ttu-id="a626a-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a626a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a626a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a626a-126">-WhatIf</span></span>
<span data-ttu-id="a626a-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a626a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a626a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a626a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a626a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a626a-129">CommonParameters</span></span>
<span data-ttu-id="a626a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a626a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a626a-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a626a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a626a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a626a-132">INPUTS</span></span>

### <span data-ttu-id="a626a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a626a-133">System.String</span></span>

## <span data-ttu-id="a626a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a626a-134">OUTPUTS</span></span>

### <span data-ttu-id="a626a-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="a626a-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a626a-136">Note</span><span class="sxs-lookup"><span data-stu-id="a626a-136">NOTES</span></span>

## <span data-ttu-id="a626a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a626a-137">RELATED LINKS</span></span>
