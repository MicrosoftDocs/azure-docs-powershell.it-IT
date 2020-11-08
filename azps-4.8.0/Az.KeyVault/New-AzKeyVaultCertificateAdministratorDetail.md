---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033447"
---
# <span data-ttu-id="9b5e7-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="9b5e7-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="9b5e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5e7-103">Crea un oggetto dettagli amministratore certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="9b5e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b5e7-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b5e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b5e7-105">DESCRIPTION</span></span>
<span data-ttu-id="9b5e7-106">Il cmdlet **New-AzKeyVaultCertificateAdministratorDetail** crea un oggetto Details dell'amministratore dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="9b5e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b5e7-107">EXAMPLES</span></span>

### <span data-ttu-id="9b5e7-108">Esempio 1: creare un oggetto Details dell'amministratore del certificato</span><span class="sxs-lookup"><span data-stu-id="9b5e7-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="9b5e7-109">Questo comando crea un oggetto dettagli amministratore del certificato in memoria e lo archivia nella variabile $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="9b5e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b5e7-110">PARAMETERS</span></span>

### <span data-ttu-id="9b5e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5e7-111">-DefaultProfile</span></span>
<span data-ttu-id="9b5e7-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9b5e7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5e7-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9b5e7-113">-EmailAddress</span></span>
<span data-ttu-id="9b5e7-114">Specifica l'indirizzo di posta elettronica per l'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="9b5e7-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="9b5e7-115">-FirstName</span></span>
<span data-ttu-id="9b5e7-116">Specifica il nome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="9b5e7-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="9b5e7-117">-LastName</span></span>
<span data-ttu-id="9b5e7-118">Specifica il cognome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="9b5e7-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9b5e7-119">-PhoneNumber</span></span>
<span data-ttu-id="9b5e7-120">Specifica il numero di telefono dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="9b5e7-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b5e7-121">-Confirm</span></span>
<span data-ttu-id="9b5e7-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b5e7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5e7-123">-WhatIf</span></span>
<span data-ttu-id="9b5e7-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b5e7-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b5e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5e7-126">CommonParameters</span></span>
<span data-ttu-id="9b5e7-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b5e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5e7-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b5e7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5e7-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b5e7-129">INPUTS</span></span>

### <span data-ttu-id="9b5e7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9b5e7-130">System.String</span></span>

## <span data-ttu-id="9b5e7-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b5e7-131">OUTPUTS</span></span>

### <span data-ttu-id="9b5e7-132">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="9b5e7-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="9b5e7-133">Note</span><span class="sxs-lookup"><span data-stu-id="9b5e7-133">NOTES</span></span>

## <span data-ttu-id="9b5e7-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b5e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b5e7-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="9b5e7-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

