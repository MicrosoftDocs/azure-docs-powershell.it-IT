---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 6844a8f4858452a1ebf9df306d75e495603703aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861285"
---
# <span data-ttu-id="019ce-101">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="019ce-101">New-AzKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="019ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="019ce-102">SYNOPSIS</span></span>
<span data-ttu-id="019ce-103">Crea un oggetto dettagli amministratore certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="019ce-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="019ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="019ce-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="019ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="019ce-105">DESCRIPTION</span></span>
<span data-ttu-id="019ce-106">Il cmdlet **New-AzKeyVaultCertificateAdministratorDetails** crea un oggetto Details dell'amministratore dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="019ce-106">The **New-AzKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="019ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="019ce-107">EXAMPLES</span></span>

### <span data-ttu-id="019ce-108">Esempio 1: creare un oggetto Details dell'amministratore del certificato</span><span class="sxs-lookup"><span data-stu-id="019ce-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="019ce-109">Questo comando crea un oggetto dettagli amministratore del certificato in memoria e lo archivia nella variabile $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="019ce-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="019ce-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="019ce-110">PARAMETERS</span></span>

### <span data-ttu-id="019ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="019ce-111">-DefaultProfile</span></span>
<span data-ttu-id="019ce-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="019ce-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019ce-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="019ce-113">-EmailAddress</span></span>
<span data-ttu-id="019ce-114">Specifica l'indirizzo di posta elettronica per l'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="019ce-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="019ce-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="019ce-115">-FirstName</span></span>
<span data-ttu-id="019ce-116">Specifica il nome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="019ce-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="019ce-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="019ce-117">-LastName</span></span>
<span data-ttu-id="019ce-118">Specifica il cognome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="019ce-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="019ce-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="019ce-119">-PhoneNumber</span></span>
<span data-ttu-id="019ce-120">Specifica il numero di telefono dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="019ce-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="019ce-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="019ce-121">-Confirm</span></span>
<span data-ttu-id="019ce-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="019ce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="019ce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="019ce-123">-WhatIf</span></span>
<span data-ttu-id="019ce-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="019ce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="019ce-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="019ce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="019ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019ce-126">CommonParameters</span></span>
<span data-ttu-id="019ce-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="019ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019ce-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="019ce-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019ce-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="019ce-129">INPUTS</span></span>

### <span data-ttu-id="019ce-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="019ce-130">None</span></span>
<span data-ttu-id="019ce-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="019ce-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="019ce-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="019ce-132">OUTPUTS</span></span>

### <span data-ttu-id="019ce-133">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="019ce-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="019ce-134">Note</span><span class="sxs-lookup"><span data-stu-id="019ce-134">NOTES</span></span>

## <span data-ttu-id="019ce-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="019ce-135">RELATED LINKS</span></span>

[<span data-ttu-id="019ce-136">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="019ce-136">New-AzKeyVaultCertificateOrganizationDetails</span></span>](./New-AzKeyVaultCertificateOrganizationDetails.md)

