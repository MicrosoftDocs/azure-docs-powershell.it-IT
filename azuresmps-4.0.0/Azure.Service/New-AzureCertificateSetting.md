---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023890"
---
# <span data-ttu-id="14349-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="14349-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="14349-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14349-102">SYNOPSIS</span></span>
<span data-ttu-id="14349-103">Crea un oggetto di impostazione del certificato per un certificato in un servizio.</span><span class="sxs-lookup"><span data-stu-id="14349-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="14349-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14349-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="14349-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14349-105">DESCRIPTION</span></span>
<span data-ttu-id="14349-106">Il cmdlet **New-AzureCertificateSetting** crea un oggetto di impostazione del certificato per un certificato che si trova in un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="14349-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="14349-107">Puoi usare un oggetto di impostazione del certificato per creare un oggetto di configurazione usando il cmdlet **Add-AzureProvisioningConfig** .</span><span class="sxs-lookup"><span data-stu-id="14349-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="14349-108">Usa un oggetto Configuration per creare una macchina virtuale usando il cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="14349-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="14349-109">Puoi usare un oggetto di impostazione del certificato per creare una macchina virtuale usando il cmdlet **New-AzureQuickVM** .</span><span class="sxs-lookup"><span data-stu-id="14349-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="14349-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14349-110">EXAMPLES</span></span>

### <span data-ttu-id="14349-111">Esempio 1: creare un oggetto di impostazione del certificato</span><span class="sxs-lookup"><span data-stu-id="14349-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="14349-112">Questo comando crea un oggetto di impostazione del certificato per un certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="14349-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="14349-113">Esempio 2: creare una macchina virtuale che usa un oggetto impostazione di configurazione</span><span class="sxs-lookup"><span data-stu-id="14349-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="14349-114">Il primo comando aggiunge il certificato ContosoCert. cer al servizio denominato ContosoService usando il cmdlet **Add-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="14349-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="14349-115">Il secondo comando crea un oggetto di impostazione del certificato e lo archivia nella variabile $CertificateSetting.</span><span class="sxs-lookup"><span data-stu-id="14349-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="14349-116">Il terzo comando ottiene un'immagine dal repository di immagini usando il cmdlet **Get-AzureVMImage** .</span><span class="sxs-lookup"><span data-stu-id="14349-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="14349-117">Questo comando Archivia l'immagine nella variabile $Image.</span><span class="sxs-lookup"><span data-stu-id="14349-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="14349-118">Il comando finale crea un oggetto di configurazione della macchina virtuale basato sull'immagine in $Image usando il cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="14349-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="14349-119">Il comando passa l'oggetto al cmdlet **Add-AzureProvisioningConfig** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="14349-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="14349-120">Questo cmdlet aggiunge le informazioni di provisioning alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="14349-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="14349-121">Il comando passa l'oggetto al cmdlet **New-AzureVM** , che crea la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="14349-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="14349-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14349-122">PARAMETERS</span></span>

### <span data-ttu-id="14349-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="14349-123">-InformationAction</span></span>
<span data-ttu-id="14349-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="14349-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="14349-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="14349-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="14349-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="14349-126">Continue</span></span>
- <span data-ttu-id="14349-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="14349-127">Ignore</span></span>
- <span data-ttu-id="14349-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="14349-128">Inquire</span></span>
- <span data-ttu-id="14349-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="14349-129">SilentlyContinue</span></span>
- <span data-ttu-id="14349-130">Stop</span><span class="sxs-lookup"><span data-stu-id="14349-130">Stop</span></span>
- <span data-ttu-id="14349-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="14349-131">Suspend</span></span>

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

### <span data-ttu-id="14349-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="14349-132">-InformationVariable</span></span>
<span data-ttu-id="14349-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="14349-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="14349-134">-StoreName</span><span class="sxs-lookup"><span data-stu-id="14349-134">-StoreName</span></span>
<span data-ttu-id="14349-135">Specifica l'archivio certificati in cui inserire il certificato.</span><span class="sxs-lookup"><span data-stu-id="14349-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="14349-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="14349-136">Valid values are:</span></span> 

- <span data-ttu-id="14349-137">AddressBook</span><span class="sxs-lookup"><span data-stu-id="14349-137">AddressBook</span></span>
- <span data-ttu-id="14349-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="14349-138">AuthRoot</span></span>
- <span data-ttu-id="14349-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="14349-139">CertificateAuthority</span></span>
- <span data-ttu-id="14349-140">Non consentiti</span><span class="sxs-lookup"><span data-stu-id="14349-140">Disallowed</span></span>
- <span data-ttu-id="14349-141">Personale</span><span class="sxs-lookup"><span data-stu-id="14349-141">My</span></span>
- <span data-ttu-id="14349-142">Radice</span><span class="sxs-lookup"><span data-stu-id="14349-142">Root</span></span>
- <span data-ttu-id="14349-143">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="14349-143">TrustedPeople</span></span>
- <span data-ttu-id="14349-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="14349-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14349-145">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="14349-145">-Thumbprint</span></span>
<span data-ttu-id="14349-146">Specifica l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="14349-146">Specifies the thumbprint of the certificate.</span></span>

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

### <span data-ttu-id="14349-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14349-147">CommonParameters</span></span>
<span data-ttu-id="14349-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14349-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14349-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14349-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14349-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14349-150">INPUTS</span></span>

## <span data-ttu-id="14349-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14349-151">OUTPUTS</span></span>

## <span data-ttu-id="14349-152">Note</span><span class="sxs-lookup"><span data-stu-id="14349-152">NOTES</span></span>

## <span data-ttu-id="14349-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14349-153">RELATED LINKS</span></span>

[<span data-ttu-id="14349-154">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="14349-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="14349-155">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="14349-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="14349-156">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="14349-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="14349-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="14349-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="14349-158">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="14349-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="14349-159">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="14349-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="14349-160">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="14349-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


