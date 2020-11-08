---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030009"
---
# <span data-ttu-id="217bd-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="217bd-101">Get-AzureVM</span></span>

## <span data-ttu-id="217bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="217bd-102">SYNOPSIS</span></span>
<span data-ttu-id="217bd-103">Recupera le informazioni da una o più macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="217bd-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="217bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="217bd-104">SYNTAX</span></span>

### <span data-ttu-id="217bd-105">ListAllVMs (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="217bd-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="217bd-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="217bd-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="217bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="217bd-107">DESCRIPTION</span></span>
<span data-ttu-id="217bd-108">Il cmdlet **Get-AzureVM** recupera le informazioni sulle macchine virtuali in uso in Azure.</span><span class="sxs-lookup"><span data-stu-id="217bd-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="217bd-109">Restituisce un oggetto con informazioni su una specifica macchina virtuale o se non viene specificata una macchina virtuale, per tutte le macchine virtuali nel servizio specificato della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="217bd-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="217bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="217bd-110">EXAMPLES</span></span>

### <span data-ttu-id="217bd-111">Esempio 1: recuperare le informazioni in una macchina virtuale specificata</span><span class="sxs-lookup"><span data-stu-id="217bd-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="217bd-112">Questo comando restituisce un oggetto con le informazioni sulla macchina virtuale VirtualMachine02 in uso nel servizio cloud di ContosoService01.</span><span class="sxs-lookup"><span data-stu-id="217bd-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="217bd-113">Esempio 2: recuperare le informazioni in tutte le macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="217bd-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="217bd-114">Questo comando Recupera un oggetto elenco con informazioni su tutte le macchine virtuali in uso nel servizio cloud di ContosoService01.</span><span class="sxs-lookup"><span data-stu-id="217bd-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="217bd-115">Esempio 3: visualizzare una tabella di stato della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="217bd-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="217bd-116">Questo comando Visualizza una tabella che mostra le macchine virtuali in uso nel servizio ContosoService01, il dominio di aggiornamento e lo stato corrente di ogni macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="217bd-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="217bd-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="217bd-117">PARAMETERS</span></span>

### <span data-ttu-id="217bd-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="217bd-118">-InformationAction</span></span>
<span data-ttu-id="217bd-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="217bd-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="217bd-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="217bd-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="217bd-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="217bd-121">Continue</span></span>
- <span data-ttu-id="217bd-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="217bd-122">Ignore</span></span>
- <span data-ttu-id="217bd-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="217bd-123">Inquire</span></span>
- <span data-ttu-id="217bd-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="217bd-124">SilentlyContinue</span></span>
- <span data-ttu-id="217bd-125">Stop</span><span class="sxs-lookup"><span data-stu-id="217bd-125">Stop</span></span>
- <span data-ttu-id="217bd-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="217bd-126">Suspend</span></span>

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

### <span data-ttu-id="217bd-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="217bd-127">-InformationVariable</span></span>
<span data-ttu-id="217bd-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="217bd-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="217bd-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="217bd-129">-Name</span></span>
<span data-ttu-id="217bd-130">Specifica il nome della macchina virtuale per cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="217bd-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="217bd-131">Se questo parametro non è disponibile, il cmdlet restituisce un oggetto elenco con informazioni su tutte le macchine virtuali nel servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="217bd-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217bd-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="217bd-132">-Profile</span></span>
<span data-ttu-id="217bd-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="217bd-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="217bd-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="217bd-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="217bd-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="217bd-135">-ServiceName</span></span>
<span data-ttu-id="217bd-136">Specifica il nome del servizio cloud per cui restituire le informazioni sulla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="217bd-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217bd-137">CommonParameters</span></span>
<span data-ttu-id="217bd-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="217bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217bd-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="217bd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217bd-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="217bd-140">INPUTS</span></span>

## <span data-ttu-id="217bd-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="217bd-141">OUTPUTS</span></span>

## <span data-ttu-id="217bd-142">Note</span><span class="sxs-lookup"><span data-stu-id="217bd-142">NOTES</span></span>

## <span data-ttu-id="217bd-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="217bd-143">RELATED LINKS</span></span>

[<span data-ttu-id="217bd-144">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="217bd-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="217bd-145">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="217bd-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="217bd-146">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="217bd-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="217bd-147">Riavviare-AzureVM</span><span class="sxs-lookup"><span data-stu-id="217bd-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="217bd-148">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="217bd-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="217bd-149">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="217bd-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="217bd-150">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="217bd-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


