---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 28a2bb0c806fa152a742c2fc9e36b150116a6352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510576"
---
# <span data-ttu-id="d88f8-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d88f8-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="d88f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d88f8-102">SYNOPSIS</span></span>
<span data-ttu-id="d88f8-103">Crea un oggetto dettagli amministratore certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="d88f8-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d88f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d88f8-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d88f8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d88f8-105">DESCRIPTION</span></span>
<span data-ttu-id="d88f8-106">Il cmdlet **New-AzureKeyVaultCertificateAdministratorDetails** crea un oggetto Details dell'amministratore dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="d88f8-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="d88f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d88f8-107">EXAMPLES</span></span>

### <span data-ttu-id="d88f8-108">Esempio 1: creare un oggetto Details dell'amministratore del certificato</span><span class="sxs-lookup"><span data-stu-id="d88f8-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="d88f8-109">Questo comando crea un oggetto dettagli amministratore del certificato in memoria e lo archivia nella variabile $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="d88f8-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="d88f8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d88f8-110">PARAMETERS</span></span>

### <span data-ttu-id="d88f8-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d88f8-111">-EmailAddress</span></span>
<span data-ttu-id="d88f8-112">Specifica l'indirizzo di posta elettronica per l'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="d88f8-112">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88f8-113">-FirstName</span><span class="sxs-lookup"><span data-stu-id="d88f8-113">-FirstName</span></span>
<span data-ttu-id="d88f8-114">Specifica il nome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="d88f8-114">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88f8-115">-LastName</span><span class="sxs-lookup"><span data-stu-id="d88f8-115">-LastName</span></span>
<span data-ttu-id="d88f8-116">Specifica il cognome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="d88f8-116">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88f8-117">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="d88f8-117">-PhoneNumber</span></span>
<span data-ttu-id="d88f8-118">Specifica il numero di telefono dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="d88f8-118">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88f8-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d88f8-119">-Confirm</span></span>
<span data-ttu-id="d88f8-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d88f8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d88f8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d88f8-121">-WhatIf</span></span>
<span data-ttu-id="d88f8-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d88f8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d88f8-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d88f8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d88f8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88f8-124">-DefaultProfile</span></span>
<span data-ttu-id="d88f8-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d88f8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d88f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88f8-126">CommonParameters</span></span>
<span data-ttu-id="d88f8-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d88f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88f8-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d88f8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88f8-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d88f8-129">INPUTS</span></span>

## <span data-ttu-id="d88f8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d88f8-130">OUTPUTS</span></span>

### <span data-ttu-id="d88f8-131">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d88f8-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="d88f8-132">Note</span><span class="sxs-lookup"><span data-stu-id="d88f8-132">NOTES</span></span>

## <span data-ttu-id="d88f8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d88f8-133">RELATED LINKS</span></span>

[<span data-ttu-id="d88f8-134">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="d88f8-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

