---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029575"
---
# <span data-ttu-id="c5e48-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c5e48-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="c5e48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5e48-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e48-103">Rimuove le estensioni del servizio cloud applicate a una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c5e48-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="c5e48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5e48-104">SYNTAX</span></span>

### <span data-ttu-id="c5e48-105">RemoveByRoles (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5e48-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c5e48-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="c5e48-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c5e48-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5e48-107">DESCRIPTION</span></span>
<span data-ttu-id="c5e48-108">Il cmdlet **Remove-AzureServiceExtension** rimuove le estensioni del servizio cloud applicate a una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c5e48-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="c5e48-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5e48-109">EXAMPLES</span></span>

### <span data-ttu-id="c5e48-110">Esempio 1: rimuovere un'estensione del servizio</span><span class="sxs-lookup"><span data-stu-id="c5e48-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="c5e48-111">Questo comando rimuove un'estensione del servizio.</span><span class="sxs-lookup"><span data-stu-id="c5e48-111">This command removes a service extension.</span></span>

### <span data-ttu-id="c5e48-112">Esempio 2: rimuovere un'estensione del servizio e disinstallare tutte le configurazioni</span><span class="sxs-lookup"><span data-stu-id="c5e48-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="c5e48-113">Questo comando rimuove un'estensione del servizio e disinstalla tutte le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="c5e48-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="c5e48-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5e48-114">PARAMETERS</span></span>

### <span data-ttu-id="c5e48-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c5e48-115">-ExtensionName</span></span>
<span data-ttu-id="c5e48-116">Specifica il nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="c5e48-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e48-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c5e48-117">-InformationAction</span></span>
<span data-ttu-id="c5e48-118">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c5e48-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c5e48-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5e48-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5e48-120">Continuare</span><span class="sxs-lookup"><span data-stu-id="c5e48-120">Continue</span></span>
- <span data-ttu-id="c5e48-121">Ignora</span><span class="sxs-lookup"><span data-stu-id="c5e48-121">Ignore</span></span>
- <span data-ttu-id="c5e48-122">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c5e48-122">Inquire</span></span>
- <span data-ttu-id="c5e48-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c5e48-123">SilentlyContinue</span></span>
- <span data-ttu-id="c5e48-124">Stop</span><span class="sxs-lookup"><span data-stu-id="c5e48-124">Stop</span></span>
- <span data-ttu-id="c5e48-125">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c5e48-125">Suspend</span></span>

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

### <span data-ttu-id="c5e48-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c5e48-126">-InformationVariable</span></span>
<span data-ttu-id="c5e48-127">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c5e48-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c5e48-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="c5e48-128">-Profile</span></span>
<span data-ttu-id="c5e48-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e48-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5e48-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c5e48-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5e48-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c5e48-131">-ProviderNamespace</span></span>
<span data-ttu-id="c5e48-132">Specifica lo spazio dei nomi del provider di estensioni.</span><span class="sxs-lookup"><span data-stu-id="c5e48-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e48-133">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="c5e48-133">-Role</span></span>
<span data-ttu-id="c5e48-134">Specifica una matrice facoltativa di ruoli per cui specificare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="c5e48-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="c5e48-135">Se non è specificata, l'estensione viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="c5e48-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="c5e48-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c5e48-136">-ServiceName</span></span>
<span data-ttu-id="c5e48-137">Specifica il nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c5e48-137">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="c5e48-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="c5e48-138">-Slot</span></span>
<span data-ttu-id="c5e48-139">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="c5e48-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="c5e48-140">I valori validi sono produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="c5e48-140">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="c5e48-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5e48-141">-UninstallConfiguration</span></span>
<span data-ttu-id="c5e48-142">Indica che questo cmdlet Disinstalla tutte le configurazioni dal servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c5e48-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e48-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e48-143">CommonParameters</span></span>
<span data-ttu-id="c5e48-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e48-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e48-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e48-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e48-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5e48-146">INPUTS</span></span>

## <span data-ttu-id="c5e48-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5e48-147">OUTPUTS</span></span>

## <span data-ttu-id="c5e48-148">Note</span><span class="sxs-lookup"><span data-stu-id="c5e48-148">NOTES</span></span>

## <span data-ttu-id="c5e48-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5e48-149">RELATED LINKS</span></span>

[<span data-ttu-id="c5e48-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c5e48-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="c5e48-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c5e48-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


