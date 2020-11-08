---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023857"
---
# <span data-ttu-id="fd12e-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="fd12e-101">New-AzureService</span></span>

## <span data-ttu-id="fd12e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd12e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd12e-103">Crea un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="fd12e-103">Creates an Azure service.</span></span>

## <span data-ttu-id="fd12e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd12e-104">SYNTAX</span></span>

### <span data-ttu-id="fd12e-105">ParameterSetAffinityGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd12e-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fd12e-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="fd12e-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fd12e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd12e-107">DESCRIPTION</span></span>
<span data-ttu-id="fd12e-108">Il cmdlet **New-AzureService** crea un nuovo servizio Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="fd12e-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="fd12e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd12e-109">EXAMPLES</span></span>

### <span data-ttu-id="fd12e-110">Esempio 1: creare un servizio</span><span class="sxs-lookup"><span data-stu-id="fd12e-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="fd12e-111">Questo comando crea un nuovo servizio denominato MySvc01 nella posizione centro sud degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="fd12e-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="fd12e-112">Esempio 2: creare un servizio in un gruppo di affinità</span><span class="sxs-lookup"><span data-stu-id="fd12e-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="fd12e-113">Questo comando crea un nuovo servizio denominato MySvc01 usando il gruppo di affinità NorthRegion.</span><span class="sxs-lookup"><span data-stu-id="fd12e-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="fd12e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd12e-114">PARAMETERS</span></span>

### <span data-ttu-id="fd12e-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="fd12e-115">-AffinityGroup</span></span>
<span data-ttu-id="fd12e-116">Specifica il gruppo di affinità associato all'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fd12e-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="fd12e-117">Se non specifichi il parametro *location* , è necessario un gruppo di affinità.</span><span class="sxs-lookup"><span data-stu-id="fd12e-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd12e-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd12e-118">-Description</span></span>
<span data-ttu-id="fd12e-119">Specifica una descrizione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="fd12e-119">Specifies a description for the service.</span></span>
<span data-ttu-id="fd12e-120">La descrizione può contenere fino a 1024 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="fd12e-120">The description may be up to 1024 characters in length.</span></span>

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

### <span data-ttu-id="fd12e-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fd12e-121">-InformationAction</span></span>
<span data-ttu-id="fd12e-122">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="fd12e-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fd12e-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd12e-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd12e-124">Continuare</span><span class="sxs-lookup"><span data-stu-id="fd12e-124">Continue</span></span>
- <span data-ttu-id="fd12e-125">Ignora</span><span class="sxs-lookup"><span data-stu-id="fd12e-125">Ignore</span></span>
- <span data-ttu-id="fd12e-126">Informarsi</span><span class="sxs-lookup"><span data-stu-id="fd12e-126">Inquire</span></span>
- <span data-ttu-id="fd12e-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fd12e-127">SilentlyContinue</span></span>
- <span data-ttu-id="fd12e-128">Stop</span><span class="sxs-lookup"><span data-stu-id="fd12e-128">Stop</span></span>
- <span data-ttu-id="fd12e-129">Sospensione</span><span class="sxs-lookup"><span data-stu-id="fd12e-129">Suspend</span></span>

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

### <span data-ttu-id="fd12e-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fd12e-130">-InformationVariable</span></span>
<span data-ttu-id="fd12e-131">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="fd12e-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fd12e-132">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="fd12e-132">-Label</span></span>
<span data-ttu-id="fd12e-133">Specifica un'etichetta per il servizio.</span><span class="sxs-lookup"><span data-stu-id="fd12e-133">Specifies a label for the service.</span></span>
<span data-ttu-id="fd12e-134">L'etichetta può contenere fino a 100 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="fd12e-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd12e-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fd12e-135">-Location</span></span>
<span data-ttu-id="fd12e-136">Specifica la posizione del servizio.</span><span class="sxs-lookup"><span data-stu-id="fd12e-136">Specifies the location for the service.</span></span>
<span data-ttu-id="fd12e-137">Se non esiste un gruppo di affinità specificato, è necessaria una posizione.</span><span class="sxs-lookup"><span data-stu-id="fd12e-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd12e-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="fd12e-138">-Profile</span></span>
<span data-ttu-id="fd12e-139">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd12e-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd12e-140">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="fd12e-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd12e-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="fd12e-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="fd12e-142">Specifica il nome di dominio completo per il DNS inverso.</span><span class="sxs-lookup"><span data-stu-id="fd12e-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd12e-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fd12e-143">-ServiceName</span></span>
<span data-ttu-id="fd12e-144">Specifica il nome del nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="fd12e-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="fd12e-145">Il nome deve essere univoco per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fd12e-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="fd12e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd12e-146">CommonParameters</span></span>
<span data-ttu-id="fd12e-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd12e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd12e-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd12e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd12e-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd12e-149">INPUTS</span></span>

## <span data-ttu-id="fd12e-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd12e-150">OUTPUTS</span></span>

## <span data-ttu-id="fd12e-151">Note</span><span class="sxs-lookup"><span data-stu-id="fd12e-151">NOTES</span></span>

## <span data-ttu-id="fd12e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd12e-152">RELATED LINKS</span></span>

[<span data-ttu-id="fd12e-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="fd12e-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="fd12e-154">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="fd12e-154">Set-AzureService</span></span>](./Set-AzureService.md)


