---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023913"
---
# <span data-ttu-id="b40e5-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="b40e5-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="b40e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b40e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b40e5-103">Aggiunge un IP pubblico a una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="b40e5-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="b40e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b40e5-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b40e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b40e5-105">DESCRIPTION</span></span>
<span data-ttu-id="b40e5-106">Il cmdlet **set-AzurePublicIP** aggiunge un IP pubblico a una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="b40e5-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="b40e5-107">Se si esegue questo cmdlet per una macchina virtuale esistente, aggiornare la macchina virtuale per implementare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="b40e5-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="b40e5-108">Puoi specificare l'etichetta di un nome di dominio per creare una voce DNS corrispondente per l'IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="b40e5-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="b40e5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b40e5-109">EXAMPLES</span></span>

### <span data-ttu-id="b40e5-110">Esempio 1: aggiungere un IP pubblico a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="b40e5-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="b40e5-111">Questo comando ottiene la macchina virtuale denominata FTPInstance nel servizio denominato FTPInAzure usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b40e5-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="b40e5-112">Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b40e5-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b40e5-113">Il cmdlet corrente aggiunge il nome IP pubblico ftpip.</span><span class="sxs-lookup"><span data-stu-id="b40e5-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="b40e5-114">Il comando passa la macchina virtuale al cmdlet **Update-AzureVM** , che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="b40e5-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="b40e5-115">Esempio 2: aggiungere un IP pubblico a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b40e5-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="b40e5-116">Questo comando crea un oggetto di configurazione della macchina virtuale usando il cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="b40e5-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="b40e5-117">Il comando passa l'oggetto al cmdlet **Add-AzureProvisioningConfig** , che fornisce una configurazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="b40e5-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="b40e5-118">Il cmdlet corrente aggiunge il nome IP pubblico ftpip.</span><span class="sxs-lookup"><span data-stu-id="b40e5-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="b40e5-119">Il comando passa la configurazione al cmdlet **New-AzureVM** , che crea la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b40e5-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="b40e5-120">Esempio 3: aggiungere un IP pubblico e un'etichetta a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="b40e5-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="b40e5-121">Questo comando ottiene la macchina virtuale denominata FTPInstance nel servizio denominato FTPInAzure usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b40e5-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="b40e5-122">Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b40e5-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b40e5-123">Il cmdlet corrente aggiunge il nome IP pubblico ftpip e l'etichetta ipname.</span><span class="sxs-lookup"><span data-stu-id="b40e5-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="b40e5-124">Il comando Aggiorna la macchina virtuale, che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="b40e5-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="b40e5-125">Esempio 4: aggiungere un IP pubblico e un'etichetta a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b40e5-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="b40e5-126">Questo comando crea un oggetto di configurazione della macchina virtuale e quindi passa tale oggetto a **Add-AzureProvisioningConfig** , che fornisce una configurazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="b40e5-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="b40e5-127">Il cmdlet corrente aggiunge il nome IP pubblico ftpip e l'etichetta ipname.</span><span class="sxs-lookup"><span data-stu-id="b40e5-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="b40e5-128">Il comando crea la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b40e5-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="b40e5-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b40e5-129">PARAMETERS</span></span>

### <span data-ttu-id="b40e5-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b40e5-130">-DomainNameLabel</span></span>
<span data-ttu-id="b40e5-131">Specifica il nome da usare per una voce DNS corrispondente per l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="b40e5-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40e5-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b40e5-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b40e5-133">Specifica il periodo di timeout inattività TCP in minuti.</span><span class="sxs-lookup"><span data-stu-id="b40e5-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40e5-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b40e5-134">-InformationAction</span></span>
<span data-ttu-id="b40e5-135">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b40e5-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b40e5-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b40e5-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b40e5-137">Continuare</span><span class="sxs-lookup"><span data-stu-id="b40e5-137">Continue</span></span>
- <span data-ttu-id="b40e5-138">Ignora</span><span class="sxs-lookup"><span data-stu-id="b40e5-138">Ignore</span></span>
- <span data-ttu-id="b40e5-139">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b40e5-139">Inquire</span></span>
- <span data-ttu-id="b40e5-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b40e5-140">SilentlyContinue</span></span>
- <span data-ttu-id="b40e5-141">Stop</span><span class="sxs-lookup"><span data-stu-id="b40e5-141">Stop</span></span>
- <span data-ttu-id="b40e5-142">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b40e5-142">Suspend</span></span>

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

### <span data-ttu-id="b40e5-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b40e5-143">-InformationVariable</span></span>
<span data-ttu-id="b40e5-144">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b40e5-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b40e5-145">-Profile</span><span class="sxs-lookup"><span data-stu-id="b40e5-145">-Profile</span></span>
<span data-ttu-id="b40e5-146">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b40e5-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b40e5-147">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b40e5-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b40e5-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="b40e5-148">-PublicIPName</span></span>
<span data-ttu-id="b40e5-149">Specifica il nome IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="b40e5-149">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40e5-150">-VM</span><span class="sxs-lookup"><span data-stu-id="b40e5-150">-VM</span></span>
<span data-ttu-id="b40e5-151">Specifica la macchina virtuale a cui questo cmdlet aggiunge IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="b40e5-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b40e5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40e5-152">CommonParameters</span></span>
<span data-ttu-id="b40e5-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40e5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40e5-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b40e5-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40e5-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b40e5-155">INPUTS</span></span>

## <span data-ttu-id="b40e5-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b40e5-156">OUTPUTS</span></span>

### <span data-ttu-id="b40e5-157">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="b40e5-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="b40e5-158">Note</span><span class="sxs-lookup"><span data-stu-id="b40e5-158">NOTES</span></span>

## <span data-ttu-id="b40e5-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b40e5-159">RELATED LINKS</span></span>

[<span data-ttu-id="b40e5-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="b40e5-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="b40e5-161">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b40e5-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="b40e5-162">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b40e5-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="b40e5-163">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="b40e5-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="b40e5-164">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="b40e5-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="b40e5-165">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b40e5-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


