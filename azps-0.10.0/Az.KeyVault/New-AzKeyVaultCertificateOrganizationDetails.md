---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863038"
---
# <span data-ttu-id="d0137-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="d0137-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="d0137-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0137-102">SYNOPSIS</span></span>
<span data-ttu-id="d0137-103">Crea un oggetto dettagli organizzazione dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="d0137-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="d0137-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0137-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0137-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0137-105">DESCRIPTION</span></span>
<span data-ttu-id="d0137-106">Il cmdlet **New-AzKeyVaultCertificateOrganizationDetails** crea un oggetto Details dell'organizzazione dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="d0137-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="d0137-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0137-107">EXAMPLES</span></span>

### <span data-ttu-id="d0137-108">Esempio 1: creare un oggetto Details dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="d0137-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="d0137-109">Il primo comando crea un oggetto Details dell'amministratore del certificato e lo archivia nella variabile $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="d0137-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="d0137-110">Il secondo comando crea un oggetto Details Organization certificate e lo archivia nella variabile $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="d0137-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="d0137-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0137-111">PARAMETERS</span></span>

### <span data-ttu-id="d0137-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d0137-112">-AdministratorDetails</span></span>
<span data-ttu-id="d0137-113">Specifica gli amministratori dell'organizzazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="d0137-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0137-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0137-114">-DefaultProfile</span></span>
<span data-ttu-id="d0137-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d0137-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0137-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d0137-116">-Id</span></span>
<span data-ttu-id="d0137-117">Specifica l'identificatore per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0137-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="d0137-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0137-118">-Confirm</span></span>
<span data-ttu-id="d0137-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0137-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0137-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0137-120">-WhatIf</span></span>
<span data-ttu-id="d0137-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0137-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0137-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0137-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0137-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0137-123">CommonParameters</span></span>
<span data-ttu-id="d0137-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0137-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0137-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0137-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0137-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0137-126">INPUTS</span></span>

### <span data-ttu-id="d0137-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d0137-127">None</span></span>
<span data-ttu-id="d0137-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d0137-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0137-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0137-129">OUTPUTS</span></span>

### <span data-ttu-id="d0137-130">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="d0137-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="d0137-131">Note</span><span class="sxs-lookup"><span data-stu-id="d0137-131">NOTES</span></span>

## <span data-ttu-id="d0137-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0137-132">RELATED LINKS</span></span>

[<span data-ttu-id="d0137-133">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d0137-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

