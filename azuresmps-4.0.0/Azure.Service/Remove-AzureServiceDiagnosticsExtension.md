---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029578"
---
# <span data-ttu-id="687ab-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="687ab-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="687ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="687ab-102">SYNOPSIS</span></span>
<span data-ttu-id="687ab-103">Rimuove l'estensione di diagnostica del servizio cloud applicata a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="687ab-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="687ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="687ab-104">SYNTAX</span></span>

### <span data-ttu-id="687ab-105">RemoveByRoles (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="687ab-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="687ab-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="687ab-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="687ab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="687ab-107">DESCRIPTION</span></span>
<span data-ttu-id="687ab-108">Il cmdlet **Remove-AzureServiceDiagnosticsExtension** rimuove l'estensione di diagnostica del servizio cloud applicata a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="687ab-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="687ab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="687ab-109">EXAMPLES</span></span>

### <span data-ttu-id="687ab-110">Esempio 1: rimuovere l'estensione di diagnostica per un servizio</span><span class="sxs-lookup"><span data-stu-id="687ab-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="687ab-111">Questo comando rimuove l'estensione di diagnostica per un ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="687ab-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="687ab-112">Esempio 2: rimuovere l'estensione di diagnostica per un servizio in un ruolo specificato</span><span class="sxs-lookup"><span data-stu-id="687ab-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="687ab-113">Questo comando rimuove l'estensione di diagnostica per un ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="687ab-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="687ab-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="687ab-114">PARAMETERS</span></span>

### <span data-ttu-id="687ab-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="687ab-115">-InformationAction</span></span>
<span data-ttu-id="687ab-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="687ab-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="687ab-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="687ab-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="687ab-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="687ab-118">Continue</span></span>
- <span data-ttu-id="687ab-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="687ab-119">Ignore</span></span>
- <span data-ttu-id="687ab-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="687ab-120">Inquire</span></span>
- <span data-ttu-id="687ab-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="687ab-121">SilentlyContinue</span></span>
- <span data-ttu-id="687ab-122">Stop</span><span class="sxs-lookup"><span data-stu-id="687ab-122">Stop</span></span>
- <span data-ttu-id="687ab-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="687ab-123">Suspend</span></span>

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

### <span data-ttu-id="687ab-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="687ab-124">-InformationVariable</span></span>
<span data-ttu-id="687ab-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="687ab-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="687ab-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="687ab-126">-Profile</span></span>
<span data-ttu-id="687ab-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="687ab-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="687ab-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="687ab-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="687ab-129">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="687ab-129">-Role</span></span>
<span data-ttu-id="687ab-130">Specifica una matrice facoltativa di ruoli per cui specificare la configurazione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="687ab-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="687ab-131">Se non specifichi questo parametro, la configurazione desktop remoto viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="687ab-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687ab-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="687ab-132">-ServiceName</span></span>
<span data-ttu-id="687ab-133">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="687ab-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="687ab-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="687ab-134">-Slot</span></span>
<span data-ttu-id="687ab-135">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="687ab-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="687ab-136">I valori validi sono produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="687ab-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="687ab-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="687ab-137">-UninstallConfiguration</span></span>
<span data-ttu-id="687ab-138">Indica che questo cmdlet Disinstalla tutte le configurazioni RDP dal servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="687ab-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687ab-139">CommonParameters</span></span>
<span data-ttu-id="687ab-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="687ab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687ab-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="687ab-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687ab-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="687ab-142">INPUTS</span></span>

## <span data-ttu-id="687ab-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="687ab-143">OUTPUTS</span></span>

## <span data-ttu-id="687ab-144">Note</span><span class="sxs-lookup"><span data-stu-id="687ab-144">NOTES</span></span>

## <span data-ttu-id="687ab-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="687ab-145">RELATED LINKS</span></span>

[<span data-ttu-id="687ab-146">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="687ab-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="687ab-147">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="687ab-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


