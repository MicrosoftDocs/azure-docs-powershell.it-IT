---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203675"
---
# <span data-ttu-id="edea5-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="edea5-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="edea5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edea5-102">SYNOPSIS</span></span>
<span data-ttu-id="edea5-103">Crea un oggetto dettagli organizzazione dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="edea5-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="edea5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edea5-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edea5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edea5-105">DESCRIPTION</span></span>
<span data-ttu-id="edea5-106">Il cmdlet **New-AzKeyVaultCertificateOrganizationDetail** crea un oggetto Details dell'organizzazione dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="edea5-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="edea5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edea5-107">EXAMPLES</span></span>

### <span data-ttu-id="edea5-108">Esempio 1: creare un oggetto Details dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="edea5-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="edea5-109">Il primo comando crea un oggetto Details dell'amministratore del certificato e lo archivia nella variabile $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="edea5-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="edea5-110">Il secondo comando crea un oggetto Details Organization certificate e lo archivia nella variabile $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="edea5-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="edea5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edea5-111">PARAMETERS</span></span>

### <span data-ttu-id="edea5-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="edea5-112">-AdministratorDetails</span></span>
<span data-ttu-id="edea5-113">Specifica gli amministratori dell'organizzazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="edea5-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="edea5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edea5-114">-DefaultProfile</span></span>
<span data-ttu-id="edea5-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="edea5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edea5-116">-ID</span><span class="sxs-lookup"><span data-stu-id="edea5-116">-Id</span></span>
<span data-ttu-id="edea5-117">Specifica l'identificatore per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="edea5-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="edea5-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="edea5-118">-Confirm</span></span>
<span data-ttu-id="edea5-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edea5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edea5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edea5-120">-WhatIf</span></span>
<span data-ttu-id="edea5-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edea5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edea5-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edea5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edea5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edea5-123">CommonParameters</span></span>
<span data-ttu-id="edea5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edea5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edea5-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edea5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edea5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edea5-126">INPUTS</span></span>

### <span data-ttu-id="edea5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="edea5-127">System.String</span></span>

### <span data-ttu-id="edea5-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateAdministratorDetails, Microsoft. Azure. PowerShell. Cmdlets. tastiera, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="edea5-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="edea5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edea5-129">OUTPUTS</span></span>

### <span data-ttu-id="edea5-130">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="edea5-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="edea5-131">Note</span><span class="sxs-lookup"><span data-stu-id="edea5-131">NOTES</span></span>

## <span data-ttu-id="edea5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edea5-132">RELATED LINKS</span></span>

[<span data-ttu-id="edea5-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="edea5-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

