---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029998"
---
# <span data-ttu-id="2fe40-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="2fe40-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="2fe40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fe40-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe40-103">Ottiene lo stato dell'estensione DSC per tutte le macchine virtuali distribuite in un servizio cloud o per una determinata macchina virtuale nel servizio.</span><span class="sxs-lookup"><span data-stu-id="2fe40-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="2fe40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fe40-104">SYNTAX</span></span>

### <span data-ttu-id="2fe40-105">GetStatusByServiceAndVMName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fe40-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2fe40-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="2fe40-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2fe40-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fe40-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe40-108">Il cmdlet **Get-AzureVMDscExtensionStatus** ottiene lo stato di estensione DSC per tutte le macchine virtuali distribuite in un servizio cloud o per una determinata macchina virtuale nel servizio.</span><span class="sxs-lookup"><span data-stu-id="2fe40-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="2fe40-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fe40-109">EXAMPLES</span></span>

### <span data-ttu-id="2fe40-110">1:</span><span class="sxs-lookup"><span data-stu-id="2fe40-110">1:</span></span>
```

```

## <span data-ttu-id="2fe40-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fe40-111">PARAMETERS</span></span>

### <span data-ttu-id="2fe40-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2fe40-112">-InformationAction</span></span>
<span data-ttu-id="2fe40-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="2fe40-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2fe40-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2fe40-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fe40-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="2fe40-115">Continue</span></span>
- <span data-ttu-id="2fe40-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="2fe40-116">Ignore</span></span>
- <span data-ttu-id="2fe40-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="2fe40-117">Inquire</span></span>
- <span data-ttu-id="2fe40-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2fe40-118">SilentlyContinue</span></span>
- <span data-ttu-id="2fe40-119">Stop</span><span class="sxs-lookup"><span data-stu-id="2fe40-119">Stop</span></span>
- <span data-ttu-id="2fe40-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="2fe40-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2fe40-121">-InformationVariable</span></span>
<span data-ttu-id="2fe40-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="2fe40-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fe40-123">-Name</span></span>
<span data-ttu-id="2fe40-124">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2fe40-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="2fe40-125">-Profile</span></span>
<span data-ttu-id="2fe40-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fe40-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2fe40-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2fe40-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2fe40-128">-ServiceName</span></span>
<span data-ttu-id="2fe40-129">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="2fe40-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-130">-VM</span><span class="sxs-lookup"><span data-stu-id="2fe40-130">-VM</span></span>
<span data-ttu-id="2fe40-131">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="2fe40-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe40-132">CommonParameters</span></span>
<span data-ttu-id="2fe40-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe40-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe40-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fe40-135">INPUTS</span></span>

## <span data-ttu-id="2fe40-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fe40-136">OUTPUTS</span></span>

### <span data-ttu-id="2fe40-137">Microsoft. WindowsAzure. Commands. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="2fe40-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="2fe40-138">Note</span><span class="sxs-lookup"><span data-stu-id="2fe40-138">NOTES</span></span>

## <span data-ttu-id="2fe40-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fe40-139">RELATED LINKS</span></span>

[<span data-ttu-id="2fe40-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2fe40-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="2fe40-141">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2fe40-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="2fe40-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2fe40-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


