---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023561"
---
# <span data-ttu-id="03b2c-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03b2c-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="03b2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="03b2c-103">Ottiene l'estensione di diagnostica del servizio cloud applicata a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="03b2c-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="03b2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03b2c-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="03b2c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="03b2c-106">Il cmdlet **Get-AzureServiceDiagnosticsExtension** Ottiene l'estensione di diagnostica del servizio cloud applicata a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="03b2c-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="03b2c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03b2c-107">EXAMPLES</span></span>

### <span data-ttu-id="03b2c-108">Esempio 1: ottenere l'estensione di diagnostica del servizio</span><span class="sxs-lookup"><span data-stu-id="03b2c-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="03b2c-109">Questo comando consente di ottenere la diagnostica del servizio per un servizio, in tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="03b2c-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="03b2c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03b2c-110">PARAMETERS</span></span>

### <span data-ttu-id="03b2c-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="03b2c-111">-InformationAction</span></span>
<span data-ttu-id="03b2c-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="03b2c-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="03b2c-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="03b2c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03b2c-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="03b2c-114">Continue</span></span>
- <span data-ttu-id="03b2c-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="03b2c-115">Ignore</span></span>
- <span data-ttu-id="03b2c-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="03b2c-116">Inquire</span></span>
- <span data-ttu-id="03b2c-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="03b2c-117">SilentlyContinue</span></span>
- <span data-ttu-id="03b2c-118">Stop</span><span class="sxs-lookup"><span data-stu-id="03b2c-118">Stop</span></span>
- <span data-ttu-id="03b2c-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="03b2c-119">Suspend</span></span>

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

### <span data-ttu-id="03b2c-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="03b2c-120">-InformationVariable</span></span>
<span data-ttu-id="03b2c-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="03b2c-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="03b2c-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="03b2c-122">-Profile</span></span>
<span data-ttu-id="03b2c-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b2c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03b2c-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="03b2c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03b2c-125">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="03b2c-125">-Role</span></span>
<span data-ttu-id="03b2c-126">Specifica una matrice di ruoli.</span><span class="sxs-lookup"><span data-stu-id="03b2c-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b2c-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="03b2c-127">-ServiceName</span></span>
<span data-ttu-id="03b2c-128">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="03b2c-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="03b2c-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="03b2c-129">-Slot</span></span>
<span data-ttu-id="03b2c-130">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="03b2c-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="03b2c-131">I valori accettabili per questo parametro sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="03b2c-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="03b2c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b2c-132">CommonParameters</span></span>
<span data-ttu-id="03b2c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b2c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b2c-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b2c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b2c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03b2c-135">INPUTS</span></span>

## <span data-ttu-id="03b2c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03b2c-136">OUTPUTS</span></span>

## <span data-ttu-id="03b2c-137">Note</span><span class="sxs-lookup"><span data-stu-id="03b2c-137">NOTES</span></span>

## <span data-ttu-id="03b2c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03b2c-138">RELATED LINKS</span></span>

[<span data-ttu-id="03b2c-139">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03b2c-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="03b2c-140">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03b2c-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


