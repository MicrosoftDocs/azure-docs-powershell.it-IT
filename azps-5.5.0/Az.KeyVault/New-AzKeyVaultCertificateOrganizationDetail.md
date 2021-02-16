---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200007"
---
# <span data-ttu-id="b048b-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="b048b-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="b048b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b048b-102">SYNOPSIS</span></span>
<span data-ttu-id="b048b-103">Crea un oggetto dettagli dell'organizzazione di certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="b048b-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="b048b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b048b-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b048b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b048b-105">DESCRIPTION</span></span>
<span data-ttu-id="b048b-106">Il cmdlet **New-AzKeyVaultCertificateOrganizationDetail** crea un oggetto dettagli organizzazione certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="b048b-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="b048b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b048b-107">EXAMPLES</span></span>

### <span data-ttu-id="b048b-108">Esempio 1: Creare un oggetto dettagli organizzazione</span><span class="sxs-lookup"><span data-stu-id="b048b-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="b048b-109">Il primo comando crea un oggetto dettagli dell'amministratore del certificato e quindi lo archivia nella $AdminDetails variabile.</span><span class="sxs-lookup"><span data-stu-id="b048b-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="b048b-110">Il secondo comando crea un oggetto dettagli organizzazione certificato e quindi lo archivia nella variabile $OrgDetails certificato.</span><span class="sxs-lookup"><span data-stu-id="b048b-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="b048b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b048b-111">PARAMETERS</span></span>

### <span data-ttu-id="b048b-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="b048b-112">-AdministratorDetails</span></span>
<span data-ttu-id="b048b-113">Specifica gli amministratori dell'organizzazione di certificati.</span><span class="sxs-lookup"><span data-stu-id="b048b-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b048b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b048b-114">-DefaultProfile</span></span>
<span data-ttu-id="b048b-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b048b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b048b-116">-Id</span><span class="sxs-lookup"><span data-stu-id="b048b-116">-Id</span></span>
<span data-ttu-id="b048b-117">Specifica l'identificatore per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b048b-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="b048b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b048b-118">-Confirm</span></span>
<span data-ttu-id="b048b-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b048b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b048b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b048b-120">-WhatIf</span></span>
<span data-ttu-id="b048b-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b048b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b048b-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b048b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b048b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b048b-123">CommonParameters</span></span>
<span data-ttu-id="b048b-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b048b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b048b-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b048b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b048b-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="b048b-126">INPUTS</span></span>

### <span data-ttu-id="b048b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b048b-127">System.String</span></span>

### <span data-ttu-id="b048b-128">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b048b-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b048b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b048b-129">OUTPUTS</span></span>

### <span data-ttu-id="b048b-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="b048b-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="b048b-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="b048b-131">NOTES</span></span>

## <span data-ttu-id="b048b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b048b-132">RELATED LINKS</span></span>

[<span data-ttu-id="b048b-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="b048b-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

