---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029574"
---
# <span data-ttu-id="e2695-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="e2695-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="e2695-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2695-102">SYNOPSIS</span></span>
<span data-ttu-id="e2695-103">Rimuove l'estensione desktop remoto del servizio cloud applicato a tutti i ruoli o ai ruoli denominati in uno slot di distribuzione specificato.</span><span class="sxs-lookup"><span data-stu-id="e2695-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="e2695-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2695-104">SYNTAX</span></span>

### <span data-ttu-id="e2695-105">RemoveByRoles (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2695-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2695-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="e2695-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e2695-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2695-107">DESCRIPTION</span></span>
<span data-ttu-id="e2695-108">Il cmdlet **Remove-AzureServiceRemoteDesktopExtension** rimuove l'estensione desktop remoto del servizio cloud applicato a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e2695-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="e2695-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2695-109">EXAMPLES</span></span>

### <span data-ttu-id="e2695-110">Esempio 1: rimuovere l'estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="e2695-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="e2695-111">Questo comando rimuove l'estensione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e2695-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="e2695-112">Esempio 2: rimuovere l'estensione desktop remoto da un ruolo specificato</span><span class="sxs-lookup"><span data-stu-id="e2695-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="e2695-113">Questo comando rimuove l'estensione desktop remoto da un ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="e2695-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="e2695-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2695-114">PARAMETERS</span></span>

### <span data-ttu-id="e2695-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e2695-115">-InformationAction</span></span>
<span data-ttu-id="e2695-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="e2695-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e2695-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2695-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2695-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="e2695-118">Continue</span></span>
- <span data-ttu-id="e2695-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="e2695-119">Ignore</span></span>
- <span data-ttu-id="e2695-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="e2695-120">Inquire</span></span>
- <span data-ttu-id="e2695-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e2695-121">SilentlyContinue</span></span>
- <span data-ttu-id="e2695-122">Stop</span><span class="sxs-lookup"><span data-stu-id="e2695-122">Stop</span></span>
- <span data-ttu-id="e2695-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="e2695-123">Suspend</span></span>

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

### <span data-ttu-id="e2695-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e2695-124">-InformationVariable</span></span>
<span data-ttu-id="e2695-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e2695-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e2695-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="e2695-126">-Profile</span></span>
<span data-ttu-id="e2695-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2695-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2695-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e2695-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2695-129">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="e2695-129">-Role</span></span>
<span data-ttu-id="e2695-130">Specifica una matrice facoltativa di ruoli per specificare la configurazione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e2695-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="e2695-131">Se non è specificata, la configurazione desktop remoto viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="e2695-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="e2695-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e2695-132">-ServiceName</span></span>
<span data-ttu-id="e2695-133">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e2695-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="e2695-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="e2695-134">-Slot</span></span>
<span data-ttu-id="e2695-135">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="e2695-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="e2695-136">I valori supportati sono "Production" o "Staging".</span><span class="sxs-lookup"><span data-stu-id="e2695-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="e2695-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2695-137">-UninstallConfiguration</span></span>
<span data-ttu-id="e2695-138">Specifica che questo cmdlet Disinstalla tutte le configurazioni RDP dal servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e2695-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="e2695-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2695-139">CommonParameters</span></span>
<span data-ttu-id="e2695-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2695-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2695-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2695-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2695-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2695-142">INPUTS</span></span>

## <span data-ttu-id="e2695-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2695-143">OUTPUTS</span></span>

## <span data-ttu-id="e2695-144">Note</span><span class="sxs-lookup"><span data-stu-id="e2695-144">NOTES</span></span>

## <span data-ttu-id="e2695-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2695-145">RELATED LINKS</span></span>

[<span data-ttu-id="e2695-146">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="e2695-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


