---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029689"
---
# <span data-ttu-id="8c045-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8c045-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="8c045-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c045-102">SYNOPSIS</span></span>
<span data-ttu-id="8c045-103">Crea un gruppo di affinità nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8c045-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="8c045-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c045-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c045-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c045-105">DESCRIPTION</span></span>
<span data-ttu-id="8c045-106">Il cmdlet **New-AzureAffinityGroup** crea un gruppo di affinità Azure nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="8c045-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="8c045-107">Un gruppo di affinità mette insieme i servizi e le relative risorse in un Data Center di Azure.</span><span class="sxs-lookup"><span data-stu-id="8c045-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="8c045-108">Il gruppo affinità raggruppa i membri per ottenere prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="8c045-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="8c045-109">Definire i gruppi di affinità a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8c045-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="8c045-110">I gruppi di affinità sono disponibili per tutti i servizi cloud o gli account di archiviazione successivi creati.</span><span class="sxs-lookup"><span data-stu-id="8c045-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="8c045-111">È possibile aggiungere servizi a un gruppo di affinità solo quando lo si crea.</span><span class="sxs-lookup"><span data-stu-id="8c045-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="8c045-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c045-112">EXAMPLES</span></span>

### <span data-ttu-id="8c045-113">Esempio 1: creare un gruppo di affinità</span><span class="sxs-lookup"><span data-stu-id="8c045-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="8c045-114">Questo comando crea un gruppo di affinità denominato South01 nell'area sud-centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="8c045-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="8c045-115">Il comando specifica un'etichetta e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="8c045-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="8c045-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c045-116">PARAMETERS</span></span>

### <span data-ttu-id="8c045-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c045-117">-Description</span></span>
<span data-ttu-id="8c045-118">Specifica una descrizione per il gruppo affinità.</span><span class="sxs-lookup"><span data-stu-id="8c045-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="8c045-119">La descrizione può contenere fino a 1024 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="8c045-119">The description may be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c045-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8c045-120">-InformationAction</span></span>
<span data-ttu-id="8c045-121">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="8c045-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8c045-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c045-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c045-123">Continuare</span><span class="sxs-lookup"><span data-stu-id="8c045-123">Continue</span></span>
- <span data-ttu-id="8c045-124">Ignora</span><span class="sxs-lookup"><span data-stu-id="8c045-124">Ignore</span></span>
- <span data-ttu-id="8c045-125">Informarsi</span><span class="sxs-lookup"><span data-stu-id="8c045-125">Inquire</span></span>
- <span data-ttu-id="8c045-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c045-126">SilentlyContinue</span></span>
- <span data-ttu-id="8c045-127">Stop</span><span class="sxs-lookup"><span data-stu-id="8c045-127">Stop</span></span>
- <span data-ttu-id="8c045-128">Sospensione</span><span class="sxs-lookup"><span data-stu-id="8c045-128">Suspend</span></span>

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

### <span data-ttu-id="8c045-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c045-129">-InformationVariable</span></span>
<span data-ttu-id="8c045-130">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="8c045-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8c045-131">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="8c045-131">-Label</span></span>
<span data-ttu-id="8c045-132">Specifica un'etichetta per il gruppo affinità.</span><span class="sxs-lookup"><span data-stu-id="8c045-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="8c045-133">L'etichetta può contenere fino a 100 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="8c045-133">The label may be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c045-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8c045-134">-Location</span></span>
<span data-ttu-id="8c045-135">Specifica la posizione geografica di Azure Data Center in cui questo cmdlet crea il gruppo affinità.</span><span class="sxs-lookup"><span data-stu-id="8c045-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c045-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c045-136">-Name</span></span>
<span data-ttu-id="8c045-137">Specifica un nome per il gruppo affinità.</span><span class="sxs-lookup"><span data-stu-id="8c045-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="8c045-138">Il nome deve essere univoco per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8c045-138">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="8c045-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="8c045-139">-Profile</span></span>
<span data-ttu-id="8c045-140">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c045-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c045-141">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8c045-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c045-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c045-142">CommonParameters</span></span>
<span data-ttu-id="8c045-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c045-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c045-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c045-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c045-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c045-145">INPUTS</span></span>

## <span data-ttu-id="8c045-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c045-146">OUTPUTS</span></span>

## <span data-ttu-id="8c045-147">Note</span><span class="sxs-lookup"><span data-stu-id="8c045-147">NOTES</span></span>

## <span data-ttu-id="8c045-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c045-148">RELATED LINKS</span></span>

[<span data-ttu-id="8c045-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8c045-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="8c045-150">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8c045-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="8c045-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8c045-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


