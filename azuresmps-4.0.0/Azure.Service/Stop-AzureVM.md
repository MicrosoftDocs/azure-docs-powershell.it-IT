---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023699"
---
# <span data-ttu-id="a22de-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a22de-101">Stop-AzureVM</span></span>

## <span data-ttu-id="a22de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a22de-102">SYNOPSIS</span></span>
<span data-ttu-id="a22de-103">Arresta una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a22de-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="a22de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a22de-104">SYNTAX</span></span>

### <span data-ttu-id="a22de-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a22de-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a22de-106">Input</span><span class="sxs-lookup"><span data-stu-id="a22de-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a22de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a22de-107">DESCRIPTION</span></span>
<span data-ttu-id="a22de-108">Il cmdlet **Stop-AzureVM** arresta una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a22de-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="a22de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a22de-109">EXAMPLES</span></span>

### <span data-ttu-id="a22de-110">Esempio 1: arrestare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a22de-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="a22de-111">Questo comando Arresta una macchina virtuale che il servizio specificato contiene.</span><span class="sxs-lookup"><span data-stu-id="a22de-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="a22de-112">Esempio 2: arrestare una macchina virtuale usando un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a22de-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="a22de-113">Questo comando Arresta una macchina virtuale che il servizio specificato contiene, usando l'oggetto macchina virtuale restituito da **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a22de-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="a22de-114">Esempio 3: arrestare una VM e conservare la VM provisioning</span><span class="sxs-lookup"><span data-stu-id="a22de-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="a22de-115">Questo comando Arresta una macchina virtuale che il servizio specificato contiene e la mantiene provisioning.</span><span class="sxs-lookup"><span data-stu-id="a22de-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="a22de-116">Esempio 4: arrestare una VM e consentire la deallocazione dell'ultima VM nella distribuzione</span><span class="sxs-lookup"><span data-stu-id="a22de-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="a22de-117">Questo comando Arresta una macchina virtuale che il servizio specificato contiene e consente la deallocazione dell'ultima macchina virtuale nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a22de-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="a22de-118">Esempio 5: arrestare più VM</span><span class="sxs-lookup"><span data-stu-id="a22de-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="a22de-119">Questo comando arresta più macchine virtuali che il servizio specificato contiene.</span><span class="sxs-lookup"><span data-stu-id="a22de-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="a22de-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a22de-120">PARAMETERS</span></span>

### <span data-ttu-id="a22de-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a22de-121">-Force</span></span>
<span data-ttu-id="a22de-122">Specifica se consentire la deallocazione dell'ultima macchina virtuale in una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a22de-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

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

### <span data-ttu-id="a22de-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a22de-123">-InformationAction</span></span>
<span data-ttu-id="a22de-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a22de-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a22de-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a22de-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a22de-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="a22de-126">Continue</span></span>
- <span data-ttu-id="a22de-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="a22de-127">Ignore</span></span>
- <span data-ttu-id="a22de-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a22de-128">Inquire</span></span>
- <span data-ttu-id="a22de-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a22de-129">SilentlyContinue</span></span>
- <span data-ttu-id="a22de-130">Stop</span><span class="sxs-lookup"><span data-stu-id="a22de-130">Stop</span></span>
- <span data-ttu-id="a22de-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a22de-131">Suspend</span></span>

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

### <span data-ttu-id="a22de-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a22de-132">-InformationVariable</span></span>
<span data-ttu-id="a22de-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a22de-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a22de-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="a22de-134">-Name</span></span>
<span data-ttu-id="a22de-135">Specifica il nome della macchina virtuale da arrestare.</span><span class="sxs-lookup"><span data-stu-id="a22de-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="a22de-136">Usa il carattere jolly per arrestare più macchine virtuali in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="a22de-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="a22de-137">Con un carattere jolly, questo cmdlet chiama l'operazione di arresto dei ruoli https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) , invece dell'operazione del ruolo Shutdown https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a22de-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22de-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="a22de-138">-Profile</span></span>
<span data-ttu-id="a22de-139">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a22de-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a22de-140">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a22de-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a22de-141">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a22de-141">-ServiceName</span></span>
<span data-ttu-id="a22de-142">Specifica il nome del servizio Azure che contiene la macchina virtuale da arrestare.</span><span class="sxs-lookup"><span data-stu-id="a22de-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="a22de-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="a22de-143">-StayProvisioned</span></span>
<span data-ttu-id="a22de-144">Specifica che questo cmdlet mantiene il provisioning della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a22de-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

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

### <span data-ttu-id="a22de-145">-VM</span><span class="sxs-lookup"><span data-stu-id="a22de-145">-VM</span></span>
<span data-ttu-id="a22de-146">Specifica un oggetto macchina virtuale che identifica la macchina virtuale da arrestare.</span><span class="sxs-lookup"><span data-stu-id="a22de-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22de-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22de-147">CommonParameters</span></span>
<span data-ttu-id="a22de-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a22de-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22de-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a22de-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22de-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a22de-150">INPUTS</span></span>

## <span data-ttu-id="a22de-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a22de-151">OUTPUTS</span></span>

## <span data-ttu-id="a22de-152">Note</span><span class="sxs-lookup"><span data-stu-id="a22de-152">NOTES</span></span>

## <span data-ttu-id="a22de-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a22de-153">RELATED LINKS</span></span>

[<span data-ttu-id="a22de-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a22de-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a22de-155">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a22de-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="a22de-156">Riavviare-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a22de-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="a22de-157">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a22de-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


