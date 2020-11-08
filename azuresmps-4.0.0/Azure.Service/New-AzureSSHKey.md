---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023940"
---
# <span data-ttu-id="e57cf-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="e57cf-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="e57cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e57cf-102">SYNOPSIS</span></span>
<span data-ttu-id="e57cf-103">Crea un oggetto chiave SSH per inserire un certificato esistente in una nuova macchina virtuale di Azure basata su Linux.</span><span class="sxs-lookup"><span data-stu-id="e57cf-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="e57cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e57cf-104">SYNTAX</span></span>

### <span data-ttu-id="e57cf-105">keyPair</span><span class="sxs-lookup"><span data-stu-id="e57cf-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e57cf-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="e57cf-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e57cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e57cf-107">DESCRIPTION</span></span>
<span data-ttu-id="e57cf-108">Il cmdlet **New-AzureSSHKey** crea un oggetto chiave SSH per un certificato già aggiunto ad Azure.</span><span class="sxs-lookup"><span data-stu-id="e57cf-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="e57cf-109">Questo oggetto chiave SSH può quindi essere usato da **New-AzureProvisioningConfig** quando si crea l'oggetto Configuration per una nuova macchina virtuale usando **New-AzureVM** o quando si crea una nuova macchina virtuale con **New-AzureQuickVM**.</span><span class="sxs-lookup"><span data-stu-id="e57cf-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="e57cf-110">Quando è incluso come parte di uno script di creazione di una macchina virtuale, questo aggiunge la chiave pubblica o la coppia di chiavi specificata in SSH alla nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e57cf-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="e57cf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e57cf-111">EXAMPLES</span></span>

### <span data-ttu-id="e57cf-112">Esempio 1: creare un oggetto di impostazione del certificato</span><span class="sxs-lookup"><span data-stu-id="e57cf-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="e57cf-113">Questo comando crea un oggetto di impostazione del certificato per un certificato esistente e quindi archivia l'oggetto in una variabile per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="e57cf-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="e57cf-114">Esempio 2: aggiungere un certificato a un servizio</span><span class="sxs-lookup"><span data-stu-id="e57cf-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="e57cf-115">Questo comando aggiunge un certificato a un servizio Azure e quindi crea una nuova macchina virtuale Linux che usa il certificato.</span><span class="sxs-lookup"><span data-stu-id="e57cf-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="e57cf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e57cf-116">PARAMETERS</span></span>

### <span data-ttu-id="e57cf-117">-Impronta digitale</span><span class="sxs-lookup"><span data-stu-id="e57cf-117">-Fingerprint</span></span>
<span data-ttu-id="e57cf-118">Specifica l'impronta digitale del certificato.</span><span class="sxs-lookup"><span data-stu-id="e57cf-118">Specifies the fingerprint of the certificate.</span></span>

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

### <span data-ttu-id="e57cf-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e57cf-119">-InformationAction</span></span>
<span data-ttu-id="e57cf-120">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="e57cf-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e57cf-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e57cf-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e57cf-122">Continuare</span><span class="sxs-lookup"><span data-stu-id="e57cf-122">Continue</span></span>
- <span data-ttu-id="e57cf-123">Ignora</span><span class="sxs-lookup"><span data-stu-id="e57cf-123">Ignore</span></span>
- <span data-ttu-id="e57cf-124">Informarsi</span><span class="sxs-lookup"><span data-stu-id="e57cf-124">Inquire</span></span>
- <span data-ttu-id="e57cf-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e57cf-125">SilentlyContinue</span></span>
- <span data-ttu-id="e57cf-126">Stop</span><span class="sxs-lookup"><span data-stu-id="e57cf-126">Stop</span></span>
- <span data-ttu-id="e57cf-127">Sospensione</span><span class="sxs-lookup"><span data-stu-id="e57cf-127">Suspend</span></span>

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

### <span data-ttu-id="e57cf-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e57cf-128">-InformationVariable</span></span>
<span data-ttu-id="e57cf-129">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e57cf-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e57cf-130">-Coppia di chiavi</span><span class="sxs-lookup"><span data-stu-id="e57cf-130">-KeyPair</span></span>
<span data-ttu-id="e57cf-131">Specifica che questo cmdlet crea un oggetto per l'inserimento di una coppia di chiavi SSH nella nuova configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e57cf-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57cf-132">-Path</span><span class="sxs-lookup"><span data-stu-id="e57cf-132">-Path</span></span>
<span data-ttu-id="e57cf-133">Specifica il percorso per archiviare la chiave pubblica SSH o la coppia di chiavi.</span><span class="sxs-lookup"><span data-stu-id="e57cf-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57cf-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="e57cf-134">-PublicKey</span></span>
<span data-ttu-id="e57cf-135">Specifica che questo cmdlet crea un oggetto per l'inserimento di una chiave pubblica SSH nella nuova configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e57cf-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57cf-136">CommonParameters</span></span>
<span data-ttu-id="e57cf-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57cf-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57cf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57cf-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e57cf-139">INPUTS</span></span>

## <span data-ttu-id="e57cf-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e57cf-140">OUTPUTS</span></span>

## <span data-ttu-id="e57cf-141">Note</span><span class="sxs-lookup"><span data-stu-id="e57cf-141">NOTES</span></span>

## <span data-ttu-id="e57cf-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e57cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="e57cf-143">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="e57cf-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="e57cf-144">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="e57cf-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="e57cf-145">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e57cf-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="e57cf-146">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="e57cf-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


