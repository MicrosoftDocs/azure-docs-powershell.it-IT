---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023882"
---
# <span data-ttu-id="a38f5-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="a38f5-101">New-AzureDns</span></span>

## <span data-ttu-id="a38f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a38f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a38f5-103">Crea un oggetto impostazioni DNS di Azure.</span><span class="sxs-lookup"><span data-stu-id="a38f5-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="a38f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a38f5-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a38f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a38f5-105">DESCRIPTION</span></span>
<span data-ttu-id="a38f5-106">Il cmdlet **New-AzureDns** crea un oggetto impostazioni DNS di Azure.</span><span class="sxs-lookup"><span data-stu-id="a38f5-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="a38f5-107">Puoi usare un oggetto impostazioni DNS quando crei una macchina virtuale usando il cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a38f5-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="a38f5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a38f5-108">EXAMPLES</span></span>

### <span data-ttu-id="a38f5-109">Esempio 1: creare un oggetto impostazioni DNS</span><span class="sxs-lookup"><span data-stu-id="a38f5-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="a38f5-110">Questo comando crea un oggetto impostazioni DNS di Azure.</span><span class="sxs-lookup"><span data-stu-id="a38f5-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="a38f5-111">Il server DNS ha l'indirizzo specificato e il nome descrittivo Dns01.</span><span class="sxs-lookup"><span data-stu-id="a38f5-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="a38f5-112">Il comando Archivia l'oggetto nella variabile $Dns per l'uso da parte del cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a38f5-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="a38f5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a38f5-113">PARAMETERS</span></span>

### <span data-ttu-id="a38f5-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a38f5-114">-InformationAction</span></span>
<span data-ttu-id="a38f5-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a38f5-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a38f5-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a38f5-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a38f5-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="a38f5-117">Continue</span></span>
- <span data-ttu-id="a38f5-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="a38f5-118">Ignore</span></span>
- <span data-ttu-id="a38f5-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a38f5-119">Inquire</span></span>
- <span data-ttu-id="a38f5-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a38f5-120">SilentlyContinue</span></span>
- <span data-ttu-id="a38f5-121">Stop</span><span class="sxs-lookup"><span data-stu-id="a38f5-121">Stop</span></span>
- <span data-ttu-id="a38f5-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a38f5-122">Suspend</span></span>

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

### <span data-ttu-id="a38f5-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a38f5-123">-InformationVariable</span></span>
<span data-ttu-id="a38f5-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a38f5-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a38f5-125">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a38f5-125">-IPAddress</span></span>
<span data-ttu-id="a38f5-126">Specifica l'indirizzo IP del server DNS.</span><span class="sxs-lookup"><span data-stu-id="a38f5-126">Specifies the IP address of the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38f5-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a38f5-127">-Name</span></span>
<span data-ttu-id="a38f5-128">Specifica un nome descrittivo per il server DNS.</span><span class="sxs-lookup"><span data-stu-id="a38f5-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="a38f5-129">Questo nome non è necessariamente un nome di dominio completo.</span><span class="sxs-lookup"><span data-stu-id="a38f5-129">This name is not necessarily a fully qualified domain name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a38f5-130">CommonParameters</span></span>
<span data-ttu-id="a38f5-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a38f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a38f5-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a38f5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a38f5-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a38f5-133">INPUTS</span></span>

## <span data-ttu-id="a38f5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a38f5-134">OUTPUTS</span></span>

## <span data-ttu-id="a38f5-135">Note</span><span class="sxs-lookup"><span data-stu-id="a38f5-135">NOTES</span></span>

## <span data-ttu-id="a38f5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a38f5-136">RELATED LINKS</span></span>

[<span data-ttu-id="a38f5-137">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="a38f5-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="a38f5-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="a38f5-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="a38f5-139">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a38f5-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="a38f5-140">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="a38f5-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="a38f5-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="a38f5-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


