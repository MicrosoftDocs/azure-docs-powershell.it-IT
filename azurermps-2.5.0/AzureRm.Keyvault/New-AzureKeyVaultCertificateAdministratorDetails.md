---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
ms.openlocfilehash: 50da8cae0af437ee86fd7462b285b812368b2508
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866682"
---
# <span data-ttu-id="e0436-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="e0436-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="e0436-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0436-102">SYNOPSIS</span></span>
<span data-ttu-id="e0436-103">Crea un oggetto dettagli amministratore certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="e0436-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0436-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0436-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0436-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0436-105">DESCRIPTION</span></span>
<span data-ttu-id="e0436-106">Il cmdlet **New-AzureKeyVaultCertificateAdministratorDetails** crea un oggetto Details dell'amministratore dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="e0436-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="e0436-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0436-107">EXAMPLES</span></span>

### <span data-ttu-id="e0436-108">Esempio 1: creare un oggetto Details dell'amministratore del certificato</span><span class="sxs-lookup"><span data-stu-id="e0436-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="e0436-109">Questo comando crea un oggetto dettagli amministratore del certificato in memoria e lo archivia nella variabile $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="e0436-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="e0436-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0436-110">PARAMETERS</span></span>

### <span data-ttu-id="e0436-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0436-111">-DefaultProfile</span></span>
<span data-ttu-id="e0436-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e0436-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0436-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e0436-113">-EmailAddress</span></span>
<span data-ttu-id="e0436-114">Specifica l'indirizzo di posta elettronica per l'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="e0436-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="e0436-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e0436-115">-FirstName</span></span>
<span data-ttu-id="e0436-116">Specifica il nome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="e0436-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="e0436-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="e0436-117">-LastName</span></span>
<span data-ttu-id="e0436-118">Specifica il cognome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="e0436-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="e0436-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="e0436-119">-PhoneNumber</span></span>
<span data-ttu-id="e0436-120">Specifica il numero di telefono dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="e0436-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="e0436-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0436-121">-Confirm</span></span>
<span data-ttu-id="e0436-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0436-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0436-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0436-123">-WhatIf</span></span>
<span data-ttu-id="e0436-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0436-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0436-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0436-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0436-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0436-126">CommonParameters</span></span>
<span data-ttu-id="e0436-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0436-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0436-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0436-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0436-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0436-129">INPUTS</span></span>

## <span data-ttu-id="e0436-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0436-130">OUTPUTS</span></span>

### <span data-ttu-id="e0436-131">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="e0436-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="e0436-132">Note</span><span class="sxs-lookup"><span data-stu-id="e0436-132">NOTES</span></span>

## <span data-ttu-id="e0436-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0436-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0436-134">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="e0436-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

