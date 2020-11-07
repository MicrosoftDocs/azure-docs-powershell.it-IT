---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 4c68470b97134019b0abf7724012f3a6fab4627f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862537"
---
# <span data-ttu-id="74f49-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="74f49-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="74f49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74f49-102">SYNOPSIS</span></span>
<span data-ttu-id="74f49-103">Aggiunge una credenziale a un'entità di servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="74f49-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="74f49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74f49-104">SYNTAX</span></span>

### <span data-ttu-id="74f49-105">SpObjectIdWithPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="74f49-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f49-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f49-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f49-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f49-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f49-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f49-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f49-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f49-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74f49-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f49-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74f49-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74f49-111">DESCRIPTION</span></span>
<span data-ttu-id="74f49-112">Il cmdlet New-AzADSpCredential può essere usato per aggiungere una nuova credenziale o per eseguire il rollforward delle credenziali per un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="74f49-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="74f49-113">L'entità servizio viene identificata fornendo l'ID oggetto o il nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="74f49-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="74f49-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74f49-114">EXAMPLES</span></span>

### <span data-ttu-id="74f49-115">Esempio 1-creare una nuova credenziale Principal del servizio usando una password generata</span><span class="sxs-lookup"><span data-stu-id="74f49-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="74f49-116">Viene aggiunta una nuova credenziale password all'entità servizio esistente con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="74f49-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="74f49-117">Esempio 2: creare una nuova credenziale Principal del servizio usando un certificato</span><span class="sxs-lookup"><span data-stu-id="74f49-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="74f49-118">Il certificato X509 pubblico con codifica Base64 fornito ("MyApp. cer") viene aggiunto all'entità servizio esistente usando il relativo nome SPN.</span><span class="sxs-lookup"><span data-stu-id="74f49-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="74f49-119">Esempio 3-creare una nuova credenziale Principal del servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="74f49-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="74f49-120">Ottiene l'entità servizio con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476" e le pipe al New-AzADSpCredential per creare una nuova credenziale principale del servizio per tale entità di servizio con una password generata.</span><span class="sxs-lookup"><span data-stu-id="74f49-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="74f49-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74f49-121">PARAMETERS</span></span>

### <span data-ttu-id="74f49-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="74f49-122">-CertValue</span></span>
<span data-ttu-id="74f49-123">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="74f49-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="74f49-124">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="74f49-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f49-125">-DefaultProfile</span></span>
<span data-ttu-id="74f49-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="74f49-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="74f49-127">-EndDate</span></span>
<span data-ttu-id="74f49-128">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="74f49-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="74f49-129">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="74f49-129">The default end date value is one year from today.</span></span> <span data-ttu-id="74f49-130">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="74f49-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="74f49-131">-ObjectId</span></span>
<span data-ttu-id="74f49-132">ID oggetto dell'entità servizio a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="74f49-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-133">-Password</span><span class="sxs-lookup"><span data-stu-id="74f49-133">-Password</span></span>
<span data-ttu-id="74f49-134">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74f49-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-135">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="74f49-135">-ServicePrincipalName</span></span>
<span data-ttu-id="74f49-136">Nome (SPN) dell'entità servizio a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="74f49-136">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-137">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="74f49-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="74f49-138">Oggetto Principal del servizio a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="74f49-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-139">-StartDate</span><span class="sxs-lookup"><span data-stu-id="74f49-139">-StartDate</span></span>
<span data-ttu-id="74f49-140">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="74f49-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="74f49-141">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="74f49-141">The default start date value is today.</span></span> <span data-ttu-id="74f49-142">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="74f49-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74f49-143">-Confirm</span></span>
<span data-ttu-id="74f49-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74f49-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f49-145">-WhatIf</span></span>
<span data-ttu-id="74f49-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74f49-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f49-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74f49-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f49-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f49-148">CommonParameters</span></span>
<span data-ttu-id="74f49-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f49-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f49-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f49-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f49-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74f49-151">INPUTS</span></span>

### <span data-ttu-id="74f49-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="74f49-152">System.Guid</span></span>

### <span data-ttu-id="74f49-153">System. String</span><span class="sxs-lookup"><span data-stu-id="74f49-153">System.String</span></span>

### <span data-ttu-id="74f49-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="74f49-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="74f49-155">Parametri: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74f49-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="74f49-156">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="74f49-156">System.Security.SecureString</span></span>

### <span data-ttu-id="74f49-157">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="74f49-157">System.DateTime</span></span>

## <span data-ttu-id="74f49-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74f49-158">OUTPUTS</span></span>

### <span data-ttu-id="74f49-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="74f49-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="74f49-160">Microsoft. Azure. Commands. resources. Models. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="74f49-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="74f49-161">Note</span><span class="sxs-lookup"><span data-stu-id="74f49-161">NOTES</span></span>

## <span data-ttu-id="74f49-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74f49-162">RELATED LINKS</span></span>

[<span data-ttu-id="74f49-163">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="74f49-163">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="74f49-164">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="74f49-164">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="74f49-165">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="74f49-165">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



