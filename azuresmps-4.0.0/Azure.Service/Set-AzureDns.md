---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029531"
---
# <span data-ttu-id="2c5db-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="2c5db-101">Set-AzureDns</span></span>

## <span data-ttu-id="2c5db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c5db-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5db-103">Modifica l'indirizzo IP di un server DNS.</span><span class="sxs-lookup"><span data-stu-id="2c5db-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="2c5db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c5db-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2c5db-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c5db-105">DESCRIPTION</span></span>
<span data-ttu-id="2c5db-106">Il cmdlet **set-AzureDns** modifica l'indirizzo IP di un server DNS per un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="2c5db-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="2c5db-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c5db-107">EXAMPLES</span></span>

### <span data-ttu-id="2c5db-108">Esempio 1: modificare l'indirizzo IP di un server DNS</span><span class="sxs-lookup"><span data-stu-id="2c5db-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="2c5db-109">Questo comando consente di modificare l'indirizzo IP del server DNS denominato Dns07 per il servizio denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="2c5db-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="2c5db-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c5db-110">PARAMETERS</span></span>

### <span data-ttu-id="2c5db-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2c5db-111">-InformationAction</span></span>
<span data-ttu-id="2c5db-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="2c5db-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2c5db-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c5db-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2c5db-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="2c5db-114">Continue</span></span>
- <span data-ttu-id="2c5db-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="2c5db-115">Ignore</span></span>
- <span data-ttu-id="2c5db-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="2c5db-116">Inquire</span></span>
- <span data-ttu-id="2c5db-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2c5db-117">SilentlyContinue</span></span>
- <span data-ttu-id="2c5db-118">Stop</span><span class="sxs-lookup"><span data-stu-id="2c5db-118">Stop</span></span>
- <span data-ttu-id="2c5db-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="2c5db-119">Suspend</span></span>

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

### <span data-ttu-id="2c5db-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2c5db-120">-InformationVariable</span></span>
<span data-ttu-id="2c5db-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="2c5db-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2c5db-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="2c5db-122">-IPAddress</span></span>
<span data-ttu-id="2c5db-123">Specifica il nuovo indirizzo IP del server DNS.</span><span class="sxs-lookup"><span data-stu-id="2c5db-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="2c5db-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c5db-124">-Name</span></span>
<span data-ttu-id="2c5db-125">Specifica il nome del server DNS che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2c5db-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2c5db-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="2c5db-126">-Profile</span></span>
<span data-ttu-id="2c5db-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c5db-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2c5db-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2c5db-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2c5db-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2c5db-129">-ServiceName</span></span>
<span data-ttu-id="2c5db-130">Specifica il nome del servizio per il quale questo cmdlet modifica l'indirizzo del server DNS.</span><span class="sxs-lookup"><span data-stu-id="2c5db-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="2c5db-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5db-131">CommonParameters</span></span>
<span data-ttu-id="2c5db-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c5db-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5db-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c5db-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5db-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c5db-134">INPUTS</span></span>

## <span data-ttu-id="2c5db-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c5db-135">OUTPUTS</span></span>

### <span data-ttu-id="2c5db-136">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="2c5db-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="2c5db-137">Note</span><span class="sxs-lookup"><span data-stu-id="2c5db-137">NOTES</span></span>

## <span data-ttu-id="2c5db-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c5db-138">RELATED LINKS</span></span>

[<span data-ttu-id="2c5db-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="2c5db-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="2c5db-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="2c5db-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="2c5db-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="2c5db-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="2c5db-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="2c5db-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


