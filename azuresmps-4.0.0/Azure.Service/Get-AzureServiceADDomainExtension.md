---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023565"
---
# <span data-ttu-id="6ce8d-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6ce8d-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="6ce8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ce8d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce8d-103">Ottiene l'estensione del dominio Active Directory (AD) del servizio cloud che si applica a tutti i ruoli o ai ruoli denominati in uno slot di distribuzione specificato.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="6ce8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ce8d-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ce8d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ce8d-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce8d-106">Il cmdlet **Get-AzureServiceADDomainExtension** Ottiene l'estensione del dominio Active Directory del servizio cloud che si applica a tutti i ruoli o ai ruoli denominati in uno slot di distribuzione specificato.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="6ce8d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ce8d-107">EXAMPLES</span></span>

### <span data-ttu-id="6ce8d-108">Esempio 1: ottenere l'estensione del dominio Active Directory per un servizio specificato</span><span class="sxs-lookup"><span data-stu-id="6ce8d-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="6ce8d-109">Questo comando consente di ottenere l'estensione del dominio Active Directory per il servizio specificato in $Svc.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="6ce8d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ce8d-110">PARAMETERS</span></span>

### <span data-ttu-id="6ce8d-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6ce8d-111">-InformationAction</span></span>
<span data-ttu-id="6ce8d-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6ce8d-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ce8d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ce8d-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="6ce8d-114">Continue</span></span>
- <span data-ttu-id="6ce8d-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="6ce8d-115">Ignore</span></span>
- <span data-ttu-id="6ce8d-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6ce8d-116">Inquire</span></span>
- <span data-ttu-id="6ce8d-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6ce8d-117">SilentlyContinue</span></span>
- <span data-ttu-id="6ce8d-118">Stop</span><span class="sxs-lookup"><span data-stu-id="6ce8d-118">Stop</span></span>
- <span data-ttu-id="6ce8d-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6ce8d-119">Suspend</span></span>

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

### <span data-ttu-id="6ce8d-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6ce8d-120">-InformationVariable</span></span>
<span data-ttu-id="6ce8d-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6ce8d-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ce8d-122">-Profile</span></span>
<span data-ttu-id="6ce8d-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ce8d-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ce8d-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6ce8d-125">-ServiceName</span></span>
<span data-ttu-id="6ce8d-126">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-126">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce8d-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="6ce8d-127">-Slot</span></span>
<span data-ttu-id="6ce8d-128">Specifica l'ambiente di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="6ce8d-129">I valori accettabili per questo parametro sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce8d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce8d-130">CommonParameters</span></span>
<span data-ttu-id="6ce8d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce8d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce8d-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce8d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce8d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ce8d-133">INPUTS</span></span>

## <span data-ttu-id="6ce8d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ce8d-134">OUTPUTS</span></span>

## <span data-ttu-id="6ce8d-135">Note</span><span class="sxs-lookup"><span data-stu-id="6ce8d-135">NOTES</span></span>

## <span data-ttu-id="6ce8d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ce8d-136">RELATED LINKS</span></span>

[<span data-ttu-id="6ce8d-137">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6ce8d-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="6ce8d-138">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6ce8d-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


