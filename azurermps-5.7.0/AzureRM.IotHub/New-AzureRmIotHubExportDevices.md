---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 2f9122b2683721aa7f92bc1695b6c314e83d76c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687913"
---
# <span data-ttu-id="1df85-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="1df85-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="1df85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1df85-102">SYNOPSIS</span></span>
<span data-ttu-id="1df85-103">Crea un nuovo processo per i dispositivi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1df85-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1df85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1df85-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1df85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1df85-105">DESCRIPTION</span></span>
<span data-ttu-id="1df85-106">Crea un nuovo processo per i dispositivi di esportazione per IotHub.</span><span class="sxs-lookup"><span data-stu-id="1df85-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="1df85-107">In questo modo verranno esportati tutti i dispositivi nel contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="1df85-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="1df85-108">Vedere l'articolo seguente su come generare l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="1df85-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="1df85-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="1df85-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="1df85-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1df85-110">EXAMPLES</span></span>

### <span data-ttu-id="1df85-111">Esempio 1 emettere una richiesta di dispositivo di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1df85-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="1df85-112">Crea una nuova richiesta di dispositivo di esportazione per il IotHub "myiothub" escluse le chiavi.</span><span class="sxs-lookup"><span data-stu-id="1df85-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="1df85-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1df85-113">PARAMETERS</span></span>

### <span data-ttu-id="1df85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df85-114">-DefaultProfile</span></span>
<span data-ttu-id="1df85-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1df85-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1df85-116">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="1df85-116">-ExportBlobContainerUri</span></span>
<span data-ttu-id="1df85-117">L'URI a cui esportare il BLOB.</span><span class="sxs-lookup"><span data-stu-id="1df85-117">The Uri to export the blob to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1df85-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1df85-118">-Name</span></span>
<span data-ttu-id="1df85-119">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="1df85-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df85-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df85-120">-ResourceGroupName</span></span>
<span data-ttu-id="1df85-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1df85-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df85-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1df85-122">-Confirm</span></span>
<span data-ttu-id="1df85-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1df85-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1df85-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1df85-124">-WhatIf</span></span>
<span data-ttu-id="1df85-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1df85-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1df85-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1df85-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1df85-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df85-127">CommonParameters</span></span>
<span data-ttu-id="1df85-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1df85-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df85-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df85-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df85-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1df85-130">INPUTS</span></span>

### <span data-ttu-id="1df85-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1df85-131">System.String</span></span>

## <span data-ttu-id="1df85-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1df85-132">OUTPUTS</span></span>

### <span data-ttu-id="1df85-133">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="1df85-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="1df85-134">Note</span><span class="sxs-lookup"><span data-stu-id="1df85-134">NOTES</span></span>

## <span data-ttu-id="1df85-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1df85-135">RELATED LINKS</span></span>

