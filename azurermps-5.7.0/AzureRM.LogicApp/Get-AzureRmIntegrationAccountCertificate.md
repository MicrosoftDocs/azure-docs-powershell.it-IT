---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 268dd2c54d9881281a5b1ee331a5b5d98892f7b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519442"
---
# <span data-ttu-id="8cb61-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8cb61-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="8cb61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cb61-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb61-103">Ottiene i certificati degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cb61-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cb61-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cb61-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cb61-105">DESCRIPTION</span></span>
<span data-ttu-id="8cb61-106">Il cmdlet **Get-AzureRmIntegrationAccountCertificate** ottiene i certificati degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cb61-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="8cb61-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="8cb61-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="8cb61-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="8cb61-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8cb61-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="8cb61-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8cb61-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="8cb61-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8cb61-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="8cb61-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8cb61-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cb61-112">EXAMPLES</span></span>

### <span data-ttu-id="8cb61-113">Esempio 1: ottenere un certificato dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="8cb61-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="8cb61-114">Questo comando ottiene il certificato dell'account di integrazione denominato IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="8cb61-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="8cb61-115">Esempio 2: ottenere i certificati degli account di integrazione tramite il nome dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="8cb61-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="8cb61-116">Questo comando consente di ottenere i certificati dell'account di integrazione per l'account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="8cb61-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="8cb61-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cb61-117">PARAMETERS</span></span>

### <span data-ttu-id="8cb61-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="8cb61-118">-CertificateName</span></span>
<span data-ttu-id="8cb61-119">Specifica il nome di un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8cb61-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb61-120">-DefaultProfile</span></span>
<span data-ttu-id="8cb61-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8cb61-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cb61-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cb61-122">-Name</span></span>
<span data-ttu-id="8cb61-123">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8cb61-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb61-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb61-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cb61-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cb61-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8cb61-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb61-126">CommonParameters</span></span>
<span data-ttu-id="8cb61-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb61-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb61-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb61-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb61-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cb61-129">INPUTS</span></span>

### <span data-ttu-id="8cb61-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8cb61-130">None</span></span>
<span data-ttu-id="8cb61-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8cb61-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cb61-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cb61-132">OUTPUTS</span></span>

### <span data-ttu-id="8cb61-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8cb61-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="8cb61-134">Note</span><span class="sxs-lookup"><span data-stu-id="8cb61-134">NOTES</span></span>

## <span data-ttu-id="8cb61-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cb61-135">RELATED LINKS</span></span>

[<span data-ttu-id="8cb61-136">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8cb61-136">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="8cb61-137">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8cb61-137">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="8cb61-138">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8cb61-138">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


