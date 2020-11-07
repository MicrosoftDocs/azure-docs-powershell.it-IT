---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: d4d7cb0a188b4c00c4ea0c07140b3360c98805aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686690"
---
# <span data-ttu-id="23e42-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="23e42-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="23e42-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23e42-102">SYNOPSIS</span></span>
<span data-ttu-id="23e42-103">Aggiunge una credenziale a un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="23e42-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23e42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23e42-104">SYNTAX</span></span>

### <span data-ttu-id="23e42-105">ApplicationObjectIdWithPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23e42-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e42-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e42-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e42-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e42-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e42-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e42-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e42-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23e42-109">DESCRIPTION</span></span>
<span data-ttu-id="23e42-110">Il cmdlet New-AzureRmADAppCredential può essere usato per aggiungere una nuova credenziale o per eseguire il rollforward delle credenziali per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="23e42-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="23e42-111">L'applicazione viene identificata fornendo l'ID oggetto applicazione o l'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="23e42-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="23e42-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23e42-112">EXAMPLES</span></span>

### <span data-ttu-id="23e42-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23e42-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="23e42-114">Viene aggiunta una nuova credenziale password a un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="23e42-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="23e42-115">In questo esempio, il valore della password fornito viene aggiunto all'applicazione usando l'ID oggetto applicazione.</span><span class="sxs-lookup"><span data-stu-id="23e42-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="23e42-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="23e42-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="23e42-117">Una nuova credenziale chiave viene aggiunta a un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="23e42-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="23e42-118">In questo esempio, il certificato di X509 pubblico con codifica Base64 fornito ("MyApp. cer") viene aggiunto all'applicazione usando applicationId.</span><span class="sxs-lookup"><span data-stu-id="23e42-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="23e42-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="23e42-119">Example 3</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="23e42-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23e42-120">PARAMETERS</span></span>

### <span data-ttu-id="23e42-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="23e42-121">-ApplicationId</span></span>
<span data-ttu-id="23e42-122">ID dell'applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="23e42-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="23e42-123">-CertValue</span></span>
<span data-ttu-id="23e42-124">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="23e42-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="23e42-125">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="23e42-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e42-126">-DefaultProfile</span></span>
<span data-ttu-id="23e42-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="23e42-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="23e42-128">-EndDate</span></span>
<span data-ttu-id="23e42-129">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="23e42-129">The effective end date of the credential usage.</span></span>
<span data-ttu-id="23e42-130">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="23e42-130">The default end date value is one year from today.</span></span> <span data-ttu-id="23e42-131">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="23e42-131">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="23e42-132">-ObjectId</span></span>
<span data-ttu-id="23e42-133">ID oggetto dell'applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="23e42-133">The object id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-134">-Password</span><span class="sxs-lookup"><span data-stu-id="23e42-134">-Password</span></span>
<span data-ttu-id="23e42-135">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="23e42-135">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="23e42-136">-StartDate</span></span>
<span data-ttu-id="23e42-137">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="23e42-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="23e42-138">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="23e42-138">The default start date value is today.</span></span>
<span data-ttu-id="23e42-139">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="23e42-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23e42-140">-Confirm</span></span>
<span data-ttu-id="23e42-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e42-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e42-142">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e42-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e42-143">CommonParameters</span></span>
<span data-ttu-id="23e42-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e42-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e42-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e42-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e42-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23e42-146">INPUTS</span></span>

### <span data-ttu-id="23e42-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="23e42-147">None</span></span>
<span data-ttu-id="23e42-148">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="23e42-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23e42-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23e42-149">OUTPUTS</span></span>

### <span data-ttu-id="23e42-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="23e42-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="23e42-151">Note</span><span class="sxs-lookup"><span data-stu-id="23e42-151">NOTES</span></span>

## <span data-ttu-id="23e42-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23e42-152">RELATED LINKS</span></span>

[<span data-ttu-id="23e42-153">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="23e42-153">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="23e42-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="23e42-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="23e42-155">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="23e42-155">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

