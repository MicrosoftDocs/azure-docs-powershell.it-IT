---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029857"
---
# <span data-ttu-id="e4309-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="e4309-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="e4309-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4309-102">SYNOPSIS</span></span>
<span data-ttu-id="e4309-103">Carica un certificato in un servizio cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4309-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="e4309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4309-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4309-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4309-105">DESCRIPTION</span></span>
<span data-ttu-id="e4309-106">Il cmdlet **Add-AzureCertificate** carica un certificato per un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="e4309-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="e4309-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4309-107">EXAMPLES</span></span>

### <span data-ttu-id="e4309-108">Esempio 1: caricare un certificato e una password</span><span class="sxs-lookup"><span data-stu-id="e4309-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="e4309-109">Questo comando carica il file di certificato ContosoCertificate. pfx in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e4309-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="e4309-110">Il comando specifica la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="e4309-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="e4309-111">Esempio 2: caricare un file di certificato</span><span class="sxs-lookup"><span data-stu-id="e4309-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="e4309-112">Questo comando carica il file di certificato ContosoCertificate. cer in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e4309-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="e4309-113">Il comando specifica la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="e4309-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="e4309-114">Esempio 3: caricare un oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="e4309-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="e4309-115">Il primo comando ottiene un certificato dall'archivio personale di un utente usando il cmdlet di base **Get-Item** di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e4309-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="e4309-116">Il comando Archivia il certificato nella variabile $Certificate.</span><span class="sxs-lookup"><span data-stu-id="e4309-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="e4309-117">Il secondo comando carica il certificato in $certificate in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e4309-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="e4309-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4309-118">PARAMETERS</span></span>

### <span data-ttu-id="e4309-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="e4309-119">-CertToDeploy</span></span>
<span data-ttu-id="e4309-120">Specifica il certificato da distribuire.</span><span class="sxs-lookup"><span data-stu-id="e4309-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="e4309-121">È possibile specificare il percorso completo di un file di certificato, ad esempio un file con estensione cer o \*.</span><span class="sxs-lookup"><span data-stu-id="e4309-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="e4309-122">estensione del nome file pfx o un oggetto certificato X. 509.</span><span class="sxs-lookup"><span data-stu-id="e4309-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4309-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e4309-123">-InformationAction</span></span>
<span data-ttu-id="e4309-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="e4309-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e4309-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e4309-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e4309-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="e4309-126">Continue</span></span>
- <span data-ttu-id="e4309-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="e4309-127">Ignore</span></span>
- <span data-ttu-id="e4309-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="e4309-128">Inquire</span></span>
- <span data-ttu-id="e4309-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e4309-129">SilentlyContinue</span></span>
- <span data-ttu-id="e4309-130">Stop</span><span class="sxs-lookup"><span data-stu-id="e4309-130">Stop</span></span>
- <span data-ttu-id="e4309-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="e4309-131">Suspend</span></span>

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

### <span data-ttu-id="e4309-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e4309-132">-InformationVariable</span></span>
<span data-ttu-id="e4309-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e4309-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e4309-134">-Password</span><span class="sxs-lookup"><span data-stu-id="e4309-134">-Password</span></span>
<span data-ttu-id="e4309-135">Specifica la password del certificato.</span><span class="sxs-lookup"><span data-stu-id="e4309-135">Specifies the certificate password.</span></span>

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

### <span data-ttu-id="e4309-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="e4309-136">-Profile</span></span>
<span data-ttu-id="e4309-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4309-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4309-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e4309-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4309-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e4309-139">-ServiceName</span></span>
<span data-ttu-id="e4309-140">Specifica il nome del servizio Azure a cui questo cmdlet aggiunge un certificato.</span><span class="sxs-lookup"><span data-stu-id="e4309-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

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

### <span data-ttu-id="e4309-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4309-141">CommonParameters</span></span>
<span data-ttu-id="e4309-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4309-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4309-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4309-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4309-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4309-144">INPUTS</span></span>

## <span data-ttu-id="e4309-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4309-145">OUTPUTS</span></span>

### <span data-ttu-id="e4309-146">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e4309-146">ManagementOperationContext</span></span>

## <span data-ttu-id="e4309-147">Note</span><span class="sxs-lookup"><span data-stu-id="e4309-147">NOTES</span></span>

## <span data-ttu-id="e4309-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4309-148">RELATED LINKS</span></span>

[<span data-ttu-id="e4309-149">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="e4309-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="e4309-150">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="e4309-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="e4309-151">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="e4309-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


