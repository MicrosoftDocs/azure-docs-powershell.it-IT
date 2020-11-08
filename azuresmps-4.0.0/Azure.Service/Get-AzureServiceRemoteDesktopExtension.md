---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023554"
---
# <span data-ttu-id="34010-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="34010-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="34010-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34010-102">SYNOPSIS</span></span>
<span data-ttu-id="34010-103">Questo cmdlet ottiene l'estensione desktop remoto del servizio cloud applicato a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="34010-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="34010-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34010-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="34010-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34010-105">DESCRIPTION</span></span>
<span data-ttu-id="34010-106">Il cmdlet **Get-AzureServiceRemoteDesktopExtension** Ottiene l'estensione desktop remoto del servizio cloud applicato a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="34010-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="34010-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34010-107">EXAMPLES</span></span>

### <span data-ttu-id="34010-108">Esempio 1: ottenere l'estensione desktop remoto per il servizio specificato</span><span class="sxs-lookup"><span data-stu-id="34010-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="34010-109">Questo comando consente di ottenere l'estensione desktop remoto per il servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="34010-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="34010-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34010-110">PARAMETERS</span></span>

### <span data-ttu-id="34010-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="34010-111">-InformationAction</span></span>
<span data-ttu-id="34010-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="34010-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="34010-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="34010-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34010-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="34010-114">Continue</span></span>
- <span data-ttu-id="34010-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="34010-115">Ignore</span></span>
- <span data-ttu-id="34010-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="34010-116">Inquire</span></span>
- <span data-ttu-id="34010-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="34010-117">SilentlyContinue</span></span>
- <span data-ttu-id="34010-118">Stop</span><span class="sxs-lookup"><span data-stu-id="34010-118">Stop</span></span>
- <span data-ttu-id="34010-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="34010-119">Suspend</span></span>

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

### <span data-ttu-id="34010-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="34010-120">-InformationVariable</span></span>
<span data-ttu-id="34010-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="34010-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="34010-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="34010-122">-Profile</span></span>
<span data-ttu-id="34010-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34010-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34010-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="34010-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34010-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="34010-125">-ServiceName</span></span>
<span data-ttu-id="34010-126">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="34010-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="34010-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="34010-127">-Slot</span></span>
<span data-ttu-id="34010-128">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="34010-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="34010-129">I valori accettabili per questo parametro sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="34010-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="34010-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34010-130">CommonParameters</span></span>
<span data-ttu-id="34010-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34010-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34010-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34010-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34010-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34010-133">INPUTS</span></span>

## <span data-ttu-id="34010-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34010-134">OUTPUTS</span></span>

## <span data-ttu-id="34010-135">Note</span><span class="sxs-lookup"><span data-stu-id="34010-135">NOTES</span></span>

## <span data-ttu-id="34010-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34010-136">RELATED LINKS</span></span>

[<span data-ttu-id="34010-137">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="34010-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


