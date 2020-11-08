---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029776"
---
# <span data-ttu-id="aef10-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="aef10-101">Get-AzureRole</span></span>

## <span data-ttu-id="aef10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aef10-102">SYNOPSIS</span></span>
<span data-ttu-id="aef10-103">Restituisce un elenco di ruoli nel servizio Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aef10-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="aef10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aef10-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="aef10-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aef10-105">DESCRIPTION</span></span>
<span data-ttu-id="aef10-106">Il cmdlet **Get-AzureRole** restituisce un oggetto List con dettagli sui ruoli nel servizio Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aef10-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="aef10-107">Se specifichi il parametro *roleName* , **Get-AzureRole** restituisce i dettagli solo per quel ruolo.</span><span class="sxs-lookup"><span data-stu-id="aef10-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="aef10-108">Se specifichi il parametro *InstanceDetails* , vengono restituiti dettagli aggiuntivi specifici dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="aef10-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="aef10-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aef10-109">EXAMPLES</span></span>

### <span data-ttu-id="aef10-110">Esempio 1: ottenere un elenco di ruoli per un servizio</span><span class="sxs-lookup"><span data-stu-id="aef10-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="aef10-111">Questo comando restituisce un oggetto con dettagli su tutti i ruoli di produzione in uso nel servizio MySvc01.</span><span class="sxs-lookup"><span data-stu-id="aef10-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="aef10-112">Esempio 2: ottenere informazioni dettagliate su un ruolo in uso in un servizio</span><span class="sxs-lookup"><span data-stu-id="aef10-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="aef10-113">Questo comando restituisce un oggetto con dettagli sul ruolo MyTestVM3, in corso nell'ambiente di gestione temporanea del servizio MySvc01.</span><span class="sxs-lookup"><span data-stu-id="aef10-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="aef10-114">Esempio 3: ottenere informazioni sull'istanza su istanze di un ruolo in uso in un servizio</span><span class="sxs-lookup"><span data-stu-id="aef10-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="aef10-115">Questo comando restituisce un oggetto con informazioni dettagliate sulle istanze del ruolo MyTestVM02 in uso nell'ambiente di produzione nel servizio MySvc01.</span><span class="sxs-lookup"><span data-stu-id="aef10-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="aef10-116">Esempio 4: ottenere una tabella delle istanze del ruolo associate a un servizio</span><span class="sxs-lookup"><span data-stu-id="aef10-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="aef10-117">Questo comando restituisce una tabella con il nome, le dimensioni e lo stato dell'istanza di tutte le istanze di ruolo in uso nell'ambiente di produzione nel servizio MySvc01.</span><span class="sxs-lookup"><span data-stu-id="aef10-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="aef10-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aef10-118">PARAMETERS</span></span>

### <span data-ttu-id="aef10-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aef10-119">-InformationAction</span></span>
<span data-ttu-id="aef10-120">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="aef10-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aef10-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aef10-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aef10-122">Continuare</span><span class="sxs-lookup"><span data-stu-id="aef10-122">Continue</span></span>
- <span data-ttu-id="aef10-123">Ignora</span><span class="sxs-lookup"><span data-stu-id="aef10-123">Ignore</span></span>
- <span data-ttu-id="aef10-124">Informarsi</span><span class="sxs-lookup"><span data-stu-id="aef10-124">Inquire</span></span>
- <span data-ttu-id="aef10-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aef10-125">SilentlyContinue</span></span>
- <span data-ttu-id="aef10-126">Stop</span><span class="sxs-lookup"><span data-stu-id="aef10-126">Stop</span></span>
- <span data-ttu-id="aef10-127">Sospensione</span><span class="sxs-lookup"><span data-stu-id="aef10-127">Suspend</span></span>

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

### <span data-ttu-id="aef10-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aef10-128">-InformationVariable</span></span>
<span data-ttu-id="aef10-129">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="aef10-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aef10-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="aef10-130">-InstanceDetails</span></span>
<span data-ttu-id="aef10-131">Specifica che questo cmdlet restituisce i dettagli sulle istanze di ogni ruolo.</span><span class="sxs-lookup"><span data-stu-id="aef10-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef10-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="aef10-132">-Profile</span></span>
<span data-ttu-id="aef10-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef10-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aef10-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="aef10-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aef10-135">-RoleName</span><span class="sxs-lookup"><span data-stu-id="aef10-135">-RoleName</span></span>
<span data-ttu-id="aef10-136">Specifica il nome del ruolo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="aef10-136">Specifies the name of the role to get.</span></span>

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

### <span data-ttu-id="aef10-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aef10-137">-ServiceName</span></span>
<span data-ttu-id="aef10-138">Specifica il nome del servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="aef10-138">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="aef10-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="aef10-139">-Slot</span></span>
<span data-ttu-id="aef10-140">Specifica l'ambiente di distribuzione di Azure.</span><span class="sxs-lookup"><span data-stu-id="aef10-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="aef10-141">I valori accettabili per questo parametro sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="aef10-141">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="aef10-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef10-142">CommonParameters</span></span>
<span data-ttu-id="aef10-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef10-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef10-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef10-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef10-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aef10-145">INPUTS</span></span>

## <span data-ttu-id="aef10-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aef10-146">OUTPUTS</span></span>

## <span data-ttu-id="aef10-147">Note</span><span class="sxs-lookup"><span data-stu-id="aef10-147">NOTES</span></span>

## <span data-ttu-id="aef10-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aef10-148">RELATED LINKS</span></span>

[<span data-ttu-id="aef10-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="aef10-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


