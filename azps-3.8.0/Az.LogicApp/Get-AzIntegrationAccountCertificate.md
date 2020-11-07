---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864686"
---
# <span data-ttu-id="d9e40-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9e40-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="d9e40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9e40-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e40-103">Ottiene i certificati degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9e40-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="d9e40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9e40-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9e40-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9e40-105">DESCRIPTION</span></span>
<span data-ttu-id="d9e40-106">Il cmdlet **Get-AzIntegrationAccountCertificate** ottiene i certificati degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9e40-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="d9e40-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="d9e40-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="d9e40-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="d9e40-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d9e40-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="d9e40-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d9e40-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="d9e40-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d9e40-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="d9e40-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d9e40-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9e40-112">EXAMPLES</span></span>

### <span data-ttu-id="d9e40-113">Esempio 1: ottenere un certificato dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="d9e40-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="d9e40-114">Questo comando ottiene il certificato dell'account di integrazione denominato IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="d9e40-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="d9e40-115">Esempio 2: ottenere i certificati degli account di integrazione tramite il nome dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="d9e40-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="d9e40-116">Questo comando consente di ottenere i certificati dell'account di integrazione per l'account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="d9e40-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="d9e40-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9e40-117">PARAMETERS</span></span>

### <span data-ttu-id="d9e40-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="d9e40-118">-CertificateName</span></span>
<span data-ttu-id="d9e40-119">Specifica il nome di un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d9e40-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e40-120">-DefaultProfile</span></span>
<span data-ttu-id="d9e40-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d9e40-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9e40-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9e40-122">-Name</span></span>
<span data-ttu-id="d9e40-123">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d9e40-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9e40-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9e40-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9e40-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d9e40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e40-126">CommonParameters</span></span>
<span data-ttu-id="d9e40-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e40-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9e40-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e40-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9e40-129">INPUTS</span></span>

### <span data-ttu-id="d9e40-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d9e40-130">System.String</span></span>

## <span data-ttu-id="d9e40-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9e40-131">OUTPUTS</span></span>

### <span data-ttu-id="d9e40-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9e40-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="d9e40-133">Note</span><span class="sxs-lookup"><span data-stu-id="d9e40-133">NOTES</span></span>

## <span data-ttu-id="d9e40-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9e40-134">RELATED LINKS</span></span>

[<span data-ttu-id="d9e40-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9e40-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="d9e40-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9e40-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="d9e40-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9e40-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


