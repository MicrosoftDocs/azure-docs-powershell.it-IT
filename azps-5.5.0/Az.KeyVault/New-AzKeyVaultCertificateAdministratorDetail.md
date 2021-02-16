---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200015"
---
# <span data-ttu-id="25b51-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="25b51-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="25b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25b51-102">SYNOPSIS</span></span>
<span data-ttu-id="25b51-103">Crea un oggetto dettagli amministratore certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="25b51-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="25b51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25b51-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b51-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25b51-105">DESCRIPTION</span></span>
<span data-ttu-id="25b51-106">Il cmdlet **New-AzKeyVaultCertificateAdministratorDetail** crea un oggetto dettagli amministratore del certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="25b51-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="25b51-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25b51-107">EXAMPLES</span></span>

### <span data-ttu-id="25b51-108">Esempio 1: Creare un oggetto dettagli amministratore del certificato</span><span class="sxs-lookup"><span data-stu-id="25b51-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="25b51-109">Questo comando crea un oggetto dettagli dell'amministratore del certificato in memoria e quindi lo archivia nella $AdminDetails variabile.</span><span class="sxs-lookup"><span data-stu-id="25b51-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="25b51-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25b51-110">PARAMETERS</span></span>

### <span data-ttu-id="25b51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b51-111">-DefaultProfile</span></span>
<span data-ttu-id="25b51-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="25b51-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25b51-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="25b51-113">-EmailAddress</span></span>
<span data-ttu-id="25b51-114">Specifica l'indirizzo di posta elettronica dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="25b51-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="25b51-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="25b51-115">-FirstName</span></span>
<span data-ttu-id="25b51-116">Specifica il nome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="25b51-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="25b51-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="25b51-117">-LastName</span></span>
<span data-ttu-id="25b51-118">Specifica il cognome dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="25b51-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="25b51-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="25b51-119">-PhoneNumber</span></span>
<span data-ttu-id="25b51-120">Specifica il numero di telefono dell'amministratore del certificato.</span><span class="sxs-lookup"><span data-stu-id="25b51-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="25b51-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25b51-121">-Confirm</span></span>
<span data-ttu-id="25b51-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25b51-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b51-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b51-123">-WhatIf</span></span>
<span data-ttu-id="25b51-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25b51-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b51-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25b51-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b51-126">CommonParameters</span></span>
<span data-ttu-id="25b51-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b51-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25b51-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b51-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="25b51-129">INPUTS</span></span>

### <span data-ttu-id="25b51-130">System.String</span><span class="sxs-lookup"><span data-stu-id="25b51-130">System.String</span></span>

## <span data-ttu-id="25b51-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25b51-131">OUTPUTS</span></span>

### <span data-ttu-id="25b51-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="25b51-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="25b51-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="25b51-133">NOTES</span></span>

## <span data-ttu-id="25b51-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25b51-134">RELATED LINKS</span></span>

[<span data-ttu-id="25b51-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="25b51-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

