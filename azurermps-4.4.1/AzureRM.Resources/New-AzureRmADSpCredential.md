---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: 814da56d9b925e19deac81dad886604d562e05e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688244"
---
# <span data-ttu-id="b96dd-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b96dd-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="b96dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b96dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b96dd-103">Aggiunge una credenziale a un'entità di servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="b96dd-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b96dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b96dd-104">SYNTAX</span></span>

### <span data-ttu-id="b96dd-105">SpObjectIdWithPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b96dd-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96dd-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b96dd-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96dd-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b96dd-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96dd-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b96dd-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b96dd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b96dd-109">DESCRIPTION</span></span>
<span data-ttu-id="b96dd-110">Il cmdlet New-AzureRmADSpCredential può essere usato per aggiungere una nuova credenziale o per eseguire il rollforward delle credenziali per un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="b96dd-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="b96dd-111">L'entità servizio viene identificata fornendo l'ID oggetto o il nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="b96dd-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="b96dd-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b96dd-112">EXAMPLES</span></span>

### <span data-ttu-id="b96dd-113">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b96dd-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password "P@ssw0rd!"
```

<span data-ttu-id="b96dd-114">Una nuova credenziale password viene aggiunta a un'entità di servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="b96dd-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="b96dd-115">In questo esempio, il valore della password fornito viene aggiunto all'entità servizio tramite il parametro objectId.</span><span class="sxs-lookup"><span data-stu-id="b96dd-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="b96dd-116">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b96dd-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="b96dd-117">Una nuova credenziale chiave viene aggiunta a un'entità di servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="b96dd-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="b96dd-118">In questo esempio, il certificato X509 pubblico con codifica Base64 ("MyApp. cer") viene aggiunto all'entità del servizio usando il relativo nome SPN.</span><span class="sxs-lookup"><span data-stu-id="b96dd-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="b96dd-119">--------------------------Esempio 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="b96dd-119">--------------------------  Example 3  --------------------------</span></span>
<span data-ttu-id="b96dd-120">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b96dd-120">@{paragraph=PS C:\\\>}</span></span>







```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="b96dd-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b96dd-121">PARAMETERS</span></span>

### <span data-ttu-id="b96dd-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b96dd-122">-CertValue</span></span>
<span data-ttu-id="b96dd-123">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="b96dd-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b96dd-124">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="b96dd-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="b96dd-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b96dd-125">-EndDate</span></span>
<span data-ttu-id="b96dd-126">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="b96dd-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b96dd-127">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="b96dd-127">The default end date value is one year from today.</span></span> <span data-ttu-id="b96dd-128">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="b96dd-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="b96dd-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b96dd-129">-ObjectId</span></span>
<span data-ttu-id="b96dd-130">ID oggetto dell'entità servizio a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="b96dd-130">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96dd-131">-Password</span><span class="sxs-lookup"><span data-stu-id="b96dd-131">-Password</span></span>
<span data-ttu-id="b96dd-132">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b96dd-132">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96dd-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b96dd-133">-ServicePrincipalName</span></span>
<span data-ttu-id="b96dd-134">Nome (SPN) dell'entità servizio a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="b96dd-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="b96dd-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b96dd-135">-StartDate</span></span>
<span data-ttu-id="b96dd-136">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="b96dd-136">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b96dd-137">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="b96dd-137">The default start date value is today.</span></span> <span data-ttu-id="b96dd-138">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="b96dd-138">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="b96dd-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b96dd-139">-Confirm</span></span>
<span data-ttu-id="b96dd-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b96dd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b96dd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b96dd-141">-WhatIf</span></span>
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

### <span data-ttu-id="b96dd-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96dd-142">-DefaultProfile</span></span>
<span data-ttu-id="b96dd-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b96dd-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96dd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96dd-144">CommonParameters</span></span>
<span data-ttu-id="b96dd-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b96dd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96dd-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b96dd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96dd-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b96dd-147">INPUTS</span></span>

## <span data-ttu-id="b96dd-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b96dd-148">OUTPUTS</span></span>

### <span data-ttu-id="b96dd-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="b96dd-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="b96dd-150">Note</span><span class="sxs-lookup"><span data-stu-id="b96dd-150">NOTES</span></span>

## <span data-ttu-id="b96dd-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b96dd-151">RELATED LINKS</span></span>

[<span data-ttu-id="b96dd-152">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b96dd-152">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="b96dd-153">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b96dd-153">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="b96dd-154">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b96dd-154">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



