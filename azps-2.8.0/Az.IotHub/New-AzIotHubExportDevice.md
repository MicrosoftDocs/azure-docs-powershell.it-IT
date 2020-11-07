---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 72c0793f75e00ec46a27cda476163f7cc0c93090
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674218"
---
# <span data-ttu-id="f2398-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="f2398-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="f2398-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2398-102">SYNOPSIS</span></span>
<span data-ttu-id="f2398-103">Crea un nuovo processo per i dispositivi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="f2398-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="f2398-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2398-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2398-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2398-105">DESCRIPTION</span></span>
<span data-ttu-id="f2398-106">Crea un nuovo processo per i dispositivi di esportazione per IotHub.</span><span class="sxs-lookup"><span data-stu-id="f2398-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="f2398-107">In questo modo verranno esportati tutti i dispositivi nel contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="f2398-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="f2398-108">Vedere l'articolo seguente su come generare l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="f2398-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="f2398-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="f2398-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="f2398-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2398-110">EXAMPLES</span></span>

### <span data-ttu-id="f2398-111">Esempio 1 emettere una richiesta di dispositivo di esportazione.</span><span class="sxs-lookup"><span data-stu-id="f2398-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="f2398-112">Crea una nuova richiesta di dispositivo di esportazione per il IotHub "myiothub" escluse le chiavi.</span><span class="sxs-lookup"><span data-stu-id="f2398-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="f2398-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2398-113">PARAMETERS</span></span>

### <span data-ttu-id="f2398-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2398-114">-DefaultProfile</span></span>
<span data-ttu-id="f2398-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f2398-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2398-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="f2398-116">-ExcludeKeys</span></span>
<span data-ttu-id="f2398-117">Consente di esportare dispositivi senza tasti.</span><span class="sxs-lookup"><span data-stu-id="f2398-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="f2398-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f2398-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="f2398-119">L'URI a cui esportare il BLOB.</span><span class="sxs-lookup"><span data-stu-id="f2398-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="f2398-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2398-120">-Name</span></span>
<span data-ttu-id="f2398-121">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="f2398-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="f2398-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2398-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2398-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f2398-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f2398-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2398-124">-Confirm</span></span>
<span data-ttu-id="f2398-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2398-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2398-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2398-126">-WhatIf</span></span>
<span data-ttu-id="f2398-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2398-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2398-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2398-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2398-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2398-129">CommonParameters</span></span>
<span data-ttu-id="f2398-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2398-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2398-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2398-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2398-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2398-132">INPUTS</span></span>

### <span data-ttu-id="f2398-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f2398-133">System.String</span></span>

## <span data-ttu-id="f2398-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2398-134">OUTPUTS</span></span>

### <span data-ttu-id="f2398-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="f2398-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="f2398-136">Note</span><span class="sxs-lookup"><span data-stu-id="f2398-136">NOTES</span></span>

## <span data-ttu-id="f2398-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2398-137">RELATED LINKS</span></span>
