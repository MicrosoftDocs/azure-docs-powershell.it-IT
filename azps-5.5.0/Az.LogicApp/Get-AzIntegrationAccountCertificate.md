---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180414"
---
# <span data-ttu-id="1fcb9-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1fcb9-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="1fcb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fcb9-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcb9-103">Recupera certificati dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="1fcb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fcb9-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fcb9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1fcb9-105">DESCRIPTION</span></span>
<span data-ttu-id="1fcb9-106">Il cmdlet **Get-AzIntegrationAccountCertificate** ottiene certificati dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="1fcb9-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="1fcb9-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1fcb9-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1fcb9-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1fcb9-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1fcb9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fcb9-112">EXAMPLES</span></span>

### <span data-ttu-id="1fcb9-113">Esempio 1: Ottenere un certificato dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="1fcb9-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="1fcb9-114">Questo comando recupera il certificato dell'account di integrazione denominato IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="1fcb9-115">Esempio 2: Ottenere certificati dell'account di integrazione in base al nome dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="1fcb9-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="1fcb9-116">Questo comando recupera i certificati dell'account di integrazione per l'account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="1fcb9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fcb9-117">PARAMETERS</span></span>

### <span data-ttu-id="1fcb9-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="1fcb9-118">-CertificateName</span></span>
<span data-ttu-id="1fcb9-119">Specifica il nome di un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="1fcb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcb9-120">-DefaultProfile</span></span>
<span data-ttu-id="1fcb9-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="1fcb9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fcb9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1fcb9-122">-Name</span></span>
<span data-ttu-id="1fcb9-123">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="1fcb9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcb9-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fcb9-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1fcb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcb9-126">CommonParameters</span></span>
<span data-ttu-id="1fcb9-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fcb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcb9-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fcb9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcb9-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="1fcb9-129">INPUTS</span></span>

### <span data-ttu-id="1fcb9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1fcb9-130">System.String</span></span>

## <span data-ttu-id="1fcb9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fcb9-131">OUTPUTS</span></span>

### <span data-ttu-id="1fcb9-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1fcb9-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="1fcb9-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="1fcb9-133">NOTES</span></span>

## <span data-ttu-id="1fcb9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fcb9-134">RELATED LINKS</span></span>

[<span data-ttu-id="1fcb9-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1fcb9-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1fcb9-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1fcb9-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1fcb9-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1fcb9-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


