---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
ms.openlocfilehash: 76e0d37ac38c8b9799093ff3a4f4ea10c2fce2f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866681"
---
# <span data-ttu-id="5bae8-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="5bae8-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="5bae8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5bae8-102">SYNOPSIS</span></span>
<span data-ttu-id="5bae8-103">Crea un oggetto dettagli organizzazione dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="5bae8-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bae8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bae8-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bae8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bae8-105">DESCRIPTION</span></span>
<span data-ttu-id="5bae8-106">Il cmdlet **New-AzureKeyVaultCertificateOrganizationDetails** crea un oggetto Details dell'organizzazione dei certificati in memoria.</span><span class="sxs-lookup"><span data-stu-id="5bae8-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="5bae8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bae8-107">EXAMPLES</span></span>

### <span data-ttu-id="5bae8-108">Esempio 1: creare un oggetto Details dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="5bae8-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="5bae8-109">Il primo comando crea un oggetto Details dell'amministratore del certificato e lo archivia nella variabile $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="5bae8-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="5bae8-110">Il secondo comando crea un oggetto Details Organization certificate e lo archivia nella variabile $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="5bae8-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="5bae8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5bae8-111">PARAMETERS</span></span>

### <span data-ttu-id="5bae8-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="5bae8-112">-AdministratorDetails</span></span>
<span data-ttu-id="5bae8-113">Specifica gli amministratori dell'organizzazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="5bae8-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="5bae8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bae8-114">-DefaultProfile</span></span>
<span data-ttu-id="5bae8-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5bae8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bae8-116">-ID</span><span class="sxs-lookup"><span data-stu-id="5bae8-116">-Id</span></span>
<span data-ttu-id="5bae8-117">Specifica l'identificatore per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5bae8-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="5bae8-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5bae8-118">-Confirm</span></span>
<span data-ttu-id="5bae8-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bae8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bae8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bae8-120">-WhatIf</span></span>
<span data-ttu-id="5bae8-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bae8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bae8-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bae8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bae8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bae8-123">CommonParameters</span></span>
<span data-ttu-id="5bae8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bae8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bae8-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bae8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bae8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5bae8-126">INPUTS</span></span>

## <span data-ttu-id="5bae8-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bae8-127">OUTPUTS</span></span>

### <span data-ttu-id="5bae8-128">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="5bae8-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="5bae8-129">Note</span><span class="sxs-lookup"><span data-stu-id="5bae8-129">NOTES</span></span>

## <span data-ttu-id="5bae8-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bae8-130">RELATED LINKS</span></span>

[<span data-ttu-id="5bae8-131">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="5bae8-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

