---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029535"
---
# <span data-ttu-id="97df1-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="97df1-101">Restart-AzureVM</span></span>

## <span data-ttu-id="97df1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97df1-102">SYNOPSIS</span></span>
<span data-ttu-id="97df1-103">Riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="97df1-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="97df1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97df1-104">SYNTAX</span></span>

### <span data-ttu-id="97df1-105">RestartByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97df1-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="97df1-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="97df1-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="97df1-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="97df1-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="97df1-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="97df1-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="97df1-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="97df1-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="97df1-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="97df1-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="97df1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97df1-111">DESCRIPTION</span></span>
<span data-ttu-id="97df1-112">Il cmdlet **Restart-AzureVM** richiede il riavvio di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="97df1-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="97df1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97df1-113">EXAMPLES</span></span>

### <span data-ttu-id="97df1-114">Esempio 1: riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="97df1-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="97df1-115">Questo comando Riavvia la macchina virtuale VirtualMachine27 in uso in Azure Service denominata Service01.</span><span class="sxs-lookup"><span data-stu-id="97df1-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="97df1-116">Esempio 2: riavviare una macchina virtuale usando un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="97df1-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="97df1-117">Questo comando Recupera l'oggetto macchina virtuale per la macchina virtuale denominato MyVM e lo riavvia.</span><span class="sxs-lookup"><span data-stu-id="97df1-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="97df1-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97df1-118">PARAMETERS</span></span>

### <span data-ttu-id="97df1-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="97df1-119">-InformationAction</span></span>
<span data-ttu-id="97df1-120">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="97df1-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="97df1-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="97df1-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97df1-122">Continuare</span><span class="sxs-lookup"><span data-stu-id="97df1-122">Continue</span></span>
- <span data-ttu-id="97df1-123">Ignora</span><span class="sxs-lookup"><span data-stu-id="97df1-123">Ignore</span></span>
- <span data-ttu-id="97df1-124">Informarsi</span><span class="sxs-lookup"><span data-stu-id="97df1-124">Inquire</span></span>
- <span data-ttu-id="97df1-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="97df1-125">SilentlyContinue</span></span>
- <span data-ttu-id="97df1-126">Stop</span><span class="sxs-lookup"><span data-stu-id="97df1-126">Stop</span></span>
- <span data-ttu-id="97df1-127">Sospensione</span><span class="sxs-lookup"><span data-stu-id="97df1-127">Suspend</span></span>

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

### <span data-ttu-id="97df1-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="97df1-128">-InformationVariable</span></span>
<span data-ttu-id="97df1-129">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="97df1-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="97df1-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="97df1-130">-InitiateMaintenance</span></span>
<span data-ttu-id="97df1-131">Avviare la manutenzione nella macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="97df1-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97df1-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="97df1-132">-Name</span></span>
<span data-ttu-id="97df1-133">Specifica il nome della macchina virtuale da riavviare.</span><span class="sxs-lookup"><span data-stu-id="97df1-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97df1-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="97df1-134">-Profile</span></span>
<span data-ttu-id="97df1-135">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97df1-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97df1-136">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="97df1-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97df1-137">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="97df1-137">-Redeploy</span></span>
<span data-ttu-id="97df1-138">Indica che il cmdlet ridistribuisce la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="97df1-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97df1-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="97df1-139">-ServiceName</span></span>
<span data-ttu-id="97df1-140">Specifica il nome del servizio Azure che contiene la macchina virtuale da riavviare.</span><span class="sxs-lookup"><span data-stu-id="97df1-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="97df1-141">-VM</span><span class="sxs-lookup"><span data-stu-id="97df1-141">-VM</span></span>
<span data-ttu-id="97df1-142">Specifica un oggetto macchina virtuale che identifica la macchina virtuale da riavviare.</span><span class="sxs-lookup"><span data-stu-id="97df1-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97df1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97df1-143">CommonParameters</span></span>
<span data-ttu-id="97df1-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97df1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97df1-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97df1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97df1-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97df1-146">INPUTS</span></span>

## <span data-ttu-id="97df1-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97df1-147">OUTPUTS</span></span>

## <span data-ttu-id="97df1-148">Note</span><span class="sxs-lookup"><span data-stu-id="97df1-148">NOTES</span></span>

## <span data-ttu-id="97df1-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97df1-149">RELATED LINKS</span></span>

[<span data-ttu-id="97df1-150">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="97df1-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="97df1-151">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="97df1-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="97df1-152">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="97df1-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="97df1-153">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="97df1-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="97df1-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="97df1-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


