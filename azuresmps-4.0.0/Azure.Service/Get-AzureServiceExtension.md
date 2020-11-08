---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023557"
---
# <span data-ttu-id="f2ea8-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="f2ea8-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="f2ea8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ea8-103">Ottiene le estensioni del servizio cloud applicate a una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="f2ea8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2ea8-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2ea8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ea8-106">Il cmdlet **Get-AzureServiceExtension** ottiene le estensioni del servizio cloud esistenti applicate a una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="f2ea8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2ea8-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ea8-108">Esempio 1: ottenere un'estensione specificata</span><span class="sxs-lookup"><span data-stu-id="f2ea8-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="f2ea8-109">Questo comando ottiene l'estensione del servizio cloud con il nome e lo spazio dei nomi specificati.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="f2ea8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2ea8-110">PARAMETERS</span></span>

### <span data-ttu-id="f2ea8-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f2ea8-111">-ExtensionName</span></span>
<span data-ttu-id="f2ea8-112">Specifica il nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-112">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ea8-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f2ea8-113">-InformationAction</span></span>
<span data-ttu-id="f2ea8-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2ea8-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2ea8-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2ea8-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="f2ea8-116">Continue</span></span>
- <span data-ttu-id="f2ea8-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="f2ea8-117">Ignore</span></span>
- <span data-ttu-id="f2ea8-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="f2ea8-118">Inquire</span></span>
- <span data-ttu-id="f2ea8-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f2ea8-119">SilentlyContinue</span></span>
- <span data-ttu-id="f2ea8-120">Stop</span><span class="sxs-lookup"><span data-stu-id="f2ea8-120">Stop</span></span>
- <span data-ttu-id="f2ea8-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="f2ea8-121">Suspend</span></span>

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

### <span data-ttu-id="f2ea8-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f2ea8-122">-InformationVariable</span></span>
<span data-ttu-id="f2ea8-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2ea8-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="f2ea8-124">-Profile</span></span>
<span data-ttu-id="f2ea8-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2ea8-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2ea8-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f2ea8-127">-ProviderNamespace</span></span>
<span data-ttu-id="f2ea8-128">Specifica lo spazio dei nomi del provider di estensioni.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-128">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ea8-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f2ea8-129">-ServiceName</span></span>
<span data-ttu-id="f2ea8-130">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-130">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="f2ea8-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="f2ea8-131">-Slot</span></span>
<span data-ttu-id="f2ea8-132">Specifica l'ambiente di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="f2ea8-133">I valori accettabili per questo parametro sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-133">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="f2ea8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ea8-134">CommonParameters</span></span>
<span data-ttu-id="f2ea8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ea8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ea8-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ea8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ea8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2ea8-137">INPUTS</span></span>

## <span data-ttu-id="f2ea8-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2ea8-138">OUTPUTS</span></span>

## <span data-ttu-id="f2ea8-139">Note</span><span class="sxs-lookup"><span data-stu-id="f2ea8-139">NOTES</span></span>

## <span data-ttu-id="f2ea8-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2ea8-140">RELATED LINKS</span></span>

[<span data-ttu-id="f2ea8-141">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="f2ea8-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="f2ea8-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="f2ea8-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


