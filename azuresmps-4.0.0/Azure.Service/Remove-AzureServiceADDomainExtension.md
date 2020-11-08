---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029588"
---
# <span data-ttu-id="da95a-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="da95a-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="da95a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da95a-102">SYNOPSIS</span></span>
<span data-ttu-id="da95a-103">Rimuove l'estensione del dominio Active Directory del servizio cloud applicata a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="da95a-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="da95a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da95a-104">SYNTAX</span></span>

### <span data-ttu-id="da95a-105">RemoveByRoles (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da95a-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="da95a-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="da95a-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="da95a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da95a-107">DESCRIPTION</span></span>
<span data-ttu-id="da95a-108">Il cmdlet **Remove-AzureServiceADDomainExtension** rimuove l'estensione del dominio Active Directory (ad) del servizio cloud applicata a tutti i ruoli o ai ruoli denominati in un determinato slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="da95a-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="da95a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da95a-109">EXAMPLES</span></span>

### <span data-ttu-id="da95a-110">Esempio 1: rimuovere un'estensione di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="da95a-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="da95a-111">Questo comando rimuove l'estensione specificata dalla variabile $Svc.</span><span class="sxs-lookup"><span data-stu-id="da95a-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="da95a-112">Esempio 2: rimuovere un'estensione del dominio Active Directory per un ruolo specificato</span><span class="sxs-lookup"><span data-stu-id="da95a-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="da95a-113">Questo comando rimuove l'estensione del servizio per il ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="da95a-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="da95a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da95a-114">PARAMETERS</span></span>

### <span data-ttu-id="da95a-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="da95a-115">-InformationAction</span></span>
<span data-ttu-id="da95a-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="da95a-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="da95a-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="da95a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="da95a-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="da95a-118">Continue</span></span>
- <span data-ttu-id="da95a-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="da95a-119">Ignore</span></span>
- <span data-ttu-id="da95a-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="da95a-120">Inquire</span></span>
- <span data-ttu-id="da95a-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="da95a-121">SilentlyContinue</span></span>
- <span data-ttu-id="da95a-122">Stop</span><span class="sxs-lookup"><span data-stu-id="da95a-122">Stop</span></span>
- <span data-ttu-id="da95a-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="da95a-123">Suspend</span></span>

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

### <span data-ttu-id="da95a-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="da95a-124">-InformationVariable</span></span>
<span data-ttu-id="da95a-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="da95a-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="da95a-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="da95a-126">-Profile</span></span>
<span data-ttu-id="da95a-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da95a-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da95a-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="da95a-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da95a-129">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="da95a-129">-Role</span></span>
<span data-ttu-id="da95a-130">Specifica una matrice facoltativa di ruoli per cui specificare la configurazione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="da95a-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="da95a-131">Se non viene specificato, la configurazione del dominio Active Directory viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="da95a-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="da95a-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="da95a-132">-ServiceName</span></span>
<span data-ttu-id="da95a-133">Specifica il nome di un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="da95a-133">Specifies the name of an Azure service.</span></span>

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

### <span data-ttu-id="da95a-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="da95a-134">-Slot</span></span>
<span data-ttu-id="da95a-135">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="da95a-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="da95a-136">I valori validi sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="da95a-136">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="da95a-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da95a-137">-UninstallConfiguration</span></span>
<span data-ttu-id="da95a-138">Indica che questo cmdlet Disinstalla tutte le configurazioni del dominio Active Directory dal servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="da95a-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

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

### <span data-ttu-id="da95a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da95a-139">CommonParameters</span></span>
<span data-ttu-id="da95a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da95a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da95a-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da95a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da95a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da95a-142">INPUTS</span></span>

## <span data-ttu-id="da95a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da95a-143">OUTPUTS</span></span>

## <span data-ttu-id="da95a-144">Note</span><span class="sxs-lookup"><span data-stu-id="da95a-144">NOTES</span></span>

## <span data-ttu-id="da95a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da95a-145">RELATED LINKS</span></span>

[<span data-ttu-id="da95a-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="da95a-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="da95a-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="da95a-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


