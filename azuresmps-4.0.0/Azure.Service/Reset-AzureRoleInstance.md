---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023438"
---
# <span data-ttu-id="84599-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="84599-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="84599-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84599-102">SYNOPSIS</span></span>
<span data-ttu-id="84599-103">Richiede un riavvio o una riimmagine di una singola istanza del ruolo o di tutte le istanze del ruolo di un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="84599-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="84599-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84599-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="84599-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84599-105">DESCRIPTION</span></span>
<span data-ttu-id="84599-106">Il cmdlet **Reset-AzureRoleInstance** richiede un riavvio o una riimmagine di un'istanza del ruolo in uso in una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="84599-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="84599-107">Questa operazione viene eseguita in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="84599-107">This operation executes synchronously.</span></span>
<span data-ttu-id="84599-108">Quando si riavvia un'istanza del ruolo, Azure accetta l'istanza offline, riavvia il sistema operativo sottostante per l'istanza e riporta l'istanza online.</span><span class="sxs-lookup"><span data-stu-id="84599-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="84599-109">Tutti i dati scritti nel disco locale vengono mantenuti durante il riavvio.</span><span class="sxs-lookup"><span data-stu-id="84599-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="84599-110">Tutti i dati in memoria vengono persi.</span><span class="sxs-lookup"><span data-stu-id="84599-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="84599-111">La riimmagine di un'istanza del ruolo comporta un comportamento diverso a seconda del tipo di ruolo.</span><span class="sxs-lookup"><span data-stu-id="84599-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="84599-112">Per un Web o un ruolo di lavoro, quando il ruolo viene reimaged, Azure prende il ruolo offline e scrive una nuova installazione del sistema operativo Azure Guest nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84599-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="84599-113">Il ruolo viene quindi riportato online.</span><span class="sxs-lookup"><span data-stu-id="84599-113">The role is then brought back online.</span></span>
<span data-ttu-id="84599-114">Per un ruolo VM, quando il ruolo viene reimaged, Azure prende il ruolo offline, riapplica l'immagine personalizzata che hai fornito e riporta il ruolo online.</span><span class="sxs-lookup"><span data-stu-id="84599-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="84599-115">Azure cerca di mantenere i dati in tutte le risorse di archiviazione locali quando il ruolo viene riimmaginato; Tuttavia, in caso di errore hardware temporaneo, la risorsa di archiviazione locale potrebbe essere persa.</span><span class="sxs-lookup"><span data-stu-id="84599-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="84599-116">Se l'applicazione richiede che i dati vengano mantenuti, è consigliabile scrivere in un'origine dati durevole, ad esempio un'unità Azure.</span><span class="sxs-lookup"><span data-stu-id="84599-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="84599-117">Tutti i dati scritti in una directory locale diversa da quella definita dalla risorsa di archiviazione locale andranno perduti quando il ruolo viene reimaged.</span><span class="sxs-lookup"><span data-stu-id="84599-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="84599-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84599-118">EXAMPLES</span></span>

### <span data-ttu-id="84599-119">Esempio 1: riavviare un'istanza del ruolo</span><span class="sxs-lookup"><span data-stu-id="84599-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="84599-120">Questo comando Riavvia l'istanza del ruolo denominata MyWebRole_IN_0 nella distribuzione di staging del servizio MySvc01.</span><span class="sxs-lookup"><span data-stu-id="84599-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="84599-121">Esempio 2: riimmagine di un'istanza del ruolo</span><span class="sxs-lookup"><span data-stu-id="84599-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="84599-122">Questo comando riimmaginerà le istanze di ruolo nella distribuzione di staging del servizio cloud di MySvc01.</span><span class="sxs-lookup"><span data-stu-id="84599-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="84599-123">Esempio 3: riimmagine di tutte le istanze del ruolo</span><span class="sxs-lookup"><span data-stu-id="84599-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="84599-124">Questo comando riimmaginerà tutte le istanze di ruolo nella distribuzione di produzione del servizio MySvc01.</span><span class="sxs-lookup"><span data-stu-id="84599-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="84599-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84599-125">PARAMETERS</span></span>

### <span data-ttu-id="84599-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="84599-126">-InformationAction</span></span>
<span data-ttu-id="84599-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="84599-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="84599-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="84599-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="84599-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="84599-129">Continue</span></span>
- <span data-ttu-id="84599-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="84599-130">Ignore</span></span>
- <span data-ttu-id="84599-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="84599-131">Inquire</span></span>
- <span data-ttu-id="84599-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="84599-132">SilentlyContinue</span></span>
- <span data-ttu-id="84599-133">Stop</span><span class="sxs-lookup"><span data-stu-id="84599-133">Stop</span></span>
- <span data-ttu-id="84599-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="84599-134">Suspend</span></span>

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

### <span data-ttu-id="84599-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="84599-135">-InformationVariable</span></span>
<span data-ttu-id="84599-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="84599-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="84599-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="84599-137">-InstanceName</span></span>
<span data-ttu-id="84599-138">Specifica il nome dell'istanza del ruolo da riassegnare o riavviare.</span><span class="sxs-lookup"><span data-stu-id="84599-138">Specifies the name of the role instance to reimage or reboot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84599-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="84599-139">-Profile</span></span>
<span data-ttu-id="84599-140">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84599-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84599-141">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="84599-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84599-142">-Riavvio</span><span class="sxs-lookup"><span data-stu-id="84599-142">-Reboot</span></span>
<span data-ttu-id="84599-143">Specifica che questo cmdlet riavvia l'istanza del ruolo specificata o, se non è specificata alcuna, tutte le istanze del ruolo.</span><span class="sxs-lookup"><span data-stu-id="84599-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="84599-144">È necessario includere un parametro *reboot* o *Reimage* , ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="84599-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84599-145">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="84599-145">-Reimage</span></span>
<span data-ttu-id="84599-146">Specifica che questo cmdlet riimmaginerà l'istanza del ruolo specificata o, se non è specificata alcuna, tutte le istanze del ruolo.</span><span class="sxs-lookup"><span data-stu-id="84599-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="84599-147">È necessario includere un parametro *reboot* o *Reimage* , ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="84599-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84599-148">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="84599-148">-ServiceName</span></span>
<span data-ttu-id="84599-149">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="84599-149">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84599-150">-Slot</span><span class="sxs-lookup"><span data-stu-id="84599-150">-Slot</span></span>
<span data-ttu-id="84599-151">Specifica l'ambiente di distribuzione in cui vengono eseguite le istanze del ruolo.</span><span class="sxs-lookup"><span data-stu-id="84599-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="84599-152">I valori validi sono: produzione e staging.</span><span class="sxs-lookup"><span data-stu-id="84599-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="84599-153">Puoi includere il parametro *DeploymentName* o *slot* , ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="84599-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84599-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84599-154">CommonParameters</span></span>
<span data-ttu-id="84599-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84599-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84599-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84599-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84599-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84599-157">INPUTS</span></span>

## <span data-ttu-id="84599-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84599-158">OUTPUTS</span></span>

## <span data-ttu-id="84599-159">Note</span><span class="sxs-lookup"><span data-stu-id="84599-159">NOTES</span></span>

## <span data-ttu-id="84599-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84599-160">RELATED LINKS</span></span>

[<span data-ttu-id="84599-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="84599-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


