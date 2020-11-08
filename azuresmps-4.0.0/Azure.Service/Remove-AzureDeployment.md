---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029627"
---
# <span data-ttu-id="c9963-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c9963-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="c9963-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9963-102">SYNOPSIS</span></span>
<span data-ttu-id="c9963-103">Elimina una distribuzione di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c9963-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="c9963-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9963-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9963-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9963-105">DESCRIPTION</span></span>
<span data-ttu-id="c9963-106">Il cmdlet **Remove-AzureDeployment** Elimina una distribuzione di un servizio cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9963-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="c9963-107">Per eliminare una distribuzione, sospenderla prima di tutto.</span><span class="sxs-lookup"><span data-stu-id="c9963-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="c9963-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9963-108">EXAMPLES</span></span>

### <span data-ttu-id="c9963-109">Esempio 1: rimuovere una distribuzione</span><span class="sxs-lookup"><span data-stu-id="c9963-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="c9963-110">Questo comando rimuove la distribuzione del servizio Azure denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="c9963-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="c9963-111">Poiché questo comando non specifica uno slot, rimuove il servizio dall'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c9963-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="c9963-112">Esempio 2: rimuovere una distribuzione e dischi rigidi virtuali</span><span class="sxs-lookup"><span data-stu-id="c9963-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="c9963-113">Questo comando rimuove la distribuzione del servizio denominato ContosoService dall'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c9963-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="c9963-114">Il comando rimuove anche i dischi rigidi virtuali sottostanti.</span><span class="sxs-lookup"><span data-stu-id="c9963-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="c9963-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9963-115">PARAMETERS</span></span>

### <span data-ttu-id="c9963-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="c9963-116">-DeleteVHD</span></span>
<span data-ttu-id="c9963-117">Specifica che questo cmdlet rimuove la distribuzione e i dischi rigidi virtuali dall'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="c9963-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9963-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c9963-118">-Force</span></span>
<span data-ttu-id="c9963-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c9963-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9963-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c9963-120">-InformationAction</span></span>
<span data-ttu-id="c9963-121">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c9963-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c9963-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9963-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9963-123">Continuare</span><span class="sxs-lookup"><span data-stu-id="c9963-123">Continue</span></span>
- <span data-ttu-id="c9963-124">Ignora</span><span class="sxs-lookup"><span data-stu-id="c9963-124">Ignore</span></span>
- <span data-ttu-id="c9963-125">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c9963-125">Inquire</span></span>
- <span data-ttu-id="c9963-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c9963-126">SilentlyContinue</span></span>
- <span data-ttu-id="c9963-127">Stop</span><span class="sxs-lookup"><span data-stu-id="c9963-127">Stop</span></span>
- <span data-ttu-id="c9963-128">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c9963-128">Suspend</span></span>

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

### <span data-ttu-id="c9963-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c9963-129">-InformationVariable</span></span>
<span data-ttu-id="c9963-130">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c9963-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c9963-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9963-131">-Profile</span></span>
<span data-ttu-id="c9963-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9963-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9963-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c9963-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9963-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c9963-134">-ServiceName</span></span>
<span data-ttu-id="c9963-135">Specifica il nome del servizio per il quale questo cmdlet elimina una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c9963-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

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

### <span data-ttu-id="c9963-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="c9963-136">-Slot</span></span>
<span data-ttu-id="c9963-137">Specifica l'ambiente di distribuzione da cui questo cmdlet elimina la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c9963-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="c9963-138">I valori validi sono: staging e produzione.</span><span class="sxs-lookup"><span data-stu-id="c9963-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="c9963-139">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="c9963-139">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9963-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9963-140">CommonParameters</span></span>
<span data-ttu-id="c9963-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9963-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9963-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9963-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9963-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9963-143">INPUTS</span></span>

## <span data-ttu-id="c9963-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9963-144">OUTPUTS</span></span>

### <span data-ttu-id="c9963-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="c9963-145">ManagementOperationContext</span></span>

## <span data-ttu-id="c9963-146">Note</span><span class="sxs-lookup"><span data-stu-id="c9963-146">NOTES</span></span>

## <span data-ttu-id="c9963-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9963-147">RELATED LINKS</span></span>

[<span data-ttu-id="c9963-148">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c9963-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="c9963-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="c9963-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="c9963-150">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c9963-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="c9963-151">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c9963-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="c9963-152">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c9963-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


