---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023692"
---
# <span data-ttu-id="4f48f-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4f48f-101">Add-AzureDns</span></span>

## <span data-ttu-id="4f48f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f48f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f48f-103">Aggiunge un server DNS a un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="4f48f-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="4f48f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f48f-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f48f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f48f-105">DESCRIPTION</span></span>
<span data-ttu-id="4f48f-106">Il cmdlet **Add-AzureDns** aggiunge un server DNS a un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="4f48f-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="4f48f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f48f-107">EXAMPLES</span></span>

### <span data-ttu-id="4f48f-108">Esempio 1: aggiungere un server DNS</span><span class="sxs-lookup"><span data-stu-id="4f48f-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="4f48f-109">Questo comando aggiunge il server DNS con l'indirizzo 10.1.2.4 a ContosoService.</span><span class="sxs-lookup"><span data-stu-id="4f48f-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="4f48f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f48f-110">PARAMETERS</span></span>

### <span data-ttu-id="4f48f-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4f48f-111">-InformationAction</span></span>
<span data-ttu-id="4f48f-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="4f48f-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f48f-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f48f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f48f-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="4f48f-114">Continue</span></span>
- <span data-ttu-id="4f48f-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="4f48f-115">Ignore</span></span>
- <span data-ttu-id="4f48f-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="4f48f-116">Inquire</span></span>
- <span data-ttu-id="4f48f-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f48f-117">SilentlyContinue</span></span>
- <span data-ttu-id="4f48f-118">Stop</span><span class="sxs-lookup"><span data-stu-id="4f48f-118">Stop</span></span>
- <span data-ttu-id="4f48f-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="4f48f-119">Suspend</span></span>

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

### <span data-ttu-id="4f48f-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f48f-120">-InformationVariable</span></span>
<span data-ttu-id="4f48f-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="4f48f-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f48f-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="4f48f-122">-IPAddress</span></span>
<span data-ttu-id="4f48f-123">Specifica l'indirizzo IP del server DNS.</span><span class="sxs-lookup"><span data-stu-id="4f48f-123">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="4f48f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f48f-124">-Name</span></span>
<span data-ttu-id="4f48f-125">Specifica un nome descrittivo per il server DNS.</span><span class="sxs-lookup"><span data-stu-id="4f48f-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="4f48f-126">Questo nome non è necessariamente un nome di dominio completo.</span><span class="sxs-lookup"><span data-stu-id="4f48f-126">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="4f48f-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="4f48f-127">-Profile</span></span>
<span data-ttu-id="4f48f-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f48f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f48f-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="4f48f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f48f-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4f48f-130">-ServiceName</span></span>
<span data-ttu-id="4f48f-131">Specifica il nome del servizio a cui questo cmdlet aggiunge il server DNS.</span><span class="sxs-lookup"><span data-stu-id="4f48f-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

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

### <span data-ttu-id="4f48f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f48f-132">CommonParameters</span></span>
<span data-ttu-id="4f48f-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f48f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f48f-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f48f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f48f-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f48f-135">INPUTS</span></span>

## <span data-ttu-id="4f48f-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f48f-136">OUTPUTS</span></span>

### <span data-ttu-id="4f48f-137">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="4f48f-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="4f48f-138">Note</span><span class="sxs-lookup"><span data-stu-id="4f48f-138">NOTES</span></span>

## <span data-ttu-id="4f48f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f48f-139">RELATED LINKS</span></span>

[<span data-ttu-id="4f48f-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4f48f-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="4f48f-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4f48f-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="4f48f-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4f48f-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="4f48f-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4f48f-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


