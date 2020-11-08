---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029793"
---
# <span data-ttu-id="a6cf3-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="a6cf3-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="a6cf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="a6cf3-103">Ottiene le informazioni IP pubbliche per una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="a6cf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6cf3-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a6cf3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="a6cf3-106">Il cmdlet **Get-AzurePublicIP** ottiene le informazioni IP pubbliche per una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="a6cf3-107">Per ottenere l'indirizzo IP dell'IP pubblico, usare il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a6cf3-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="a6cf3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6cf3-108">EXAMPLES</span></span>

### <span data-ttu-id="a6cf3-109">Esempio 1: ottenere la configurazione IP pubblica</span><span class="sxs-lookup"><span data-stu-id="a6cf3-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="a6cf3-110">Questo comando ottiene la macchina virtuale denominata FTPInstance nel servizio denominato FTPInAzure usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a6cf3-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a6cf3-111">Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a6cf3-112">Il cmdlet corrente ottiene la configurazione IP pubblica dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="a6cf3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6cf3-113">PARAMETERS</span></span>

### <span data-ttu-id="a6cf3-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a6cf3-114">-InformationAction</span></span>
<span data-ttu-id="a6cf3-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a6cf3-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6cf3-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a6cf3-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="a6cf3-117">Continue</span></span>
- <span data-ttu-id="a6cf3-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="a6cf3-118">Ignore</span></span>
- <span data-ttu-id="a6cf3-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a6cf3-119">Inquire</span></span>
- <span data-ttu-id="a6cf3-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a6cf3-120">SilentlyContinue</span></span>
- <span data-ttu-id="a6cf3-121">Stop</span><span class="sxs-lookup"><span data-stu-id="a6cf3-121">Stop</span></span>
- <span data-ttu-id="a6cf3-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a6cf3-122">Suspend</span></span>

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

### <span data-ttu-id="a6cf3-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a6cf3-123">-InformationVariable</span></span>
<span data-ttu-id="a6cf3-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a6cf3-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="a6cf3-125">-Profile</span></span>
<span data-ttu-id="a6cf3-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a6cf3-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6cf3-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="a6cf3-128">-PublicIPName</span></span>
<span data-ttu-id="a6cf3-129">Specifica il nome IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf3-130">-VM</span><span class="sxs-lookup"><span data-stu-id="a6cf3-130">-VM</span></span>
<span data-ttu-id="a6cf3-131">Specifica la macchina virtuale per cui questo cmdlet ottiene la configurazione IP pubblica.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6cf3-132">CommonParameters</span></span>
<span data-ttu-id="a6cf3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6cf3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6cf3-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6cf3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6cf3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6cf3-135">INPUTS</span></span>

## <span data-ttu-id="a6cf3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6cf3-136">OUTPUTS</span></span>

### <span data-ttu-id="a6cf3-137">Microsoft. WindowsAzure. Commands. ServiceManagement. AssignPublicIPCollection</span><span class="sxs-lookup"><span data-stu-id="a6cf3-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="a6cf3-138">Note</span><span class="sxs-lookup"><span data-stu-id="a6cf3-138">NOTES</span></span>

## <span data-ttu-id="a6cf3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6cf3-139">RELATED LINKS</span></span>

[<span data-ttu-id="a6cf3-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a6cf3-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a6cf3-141">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="a6cf3-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="a6cf3-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="a6cf3-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)


