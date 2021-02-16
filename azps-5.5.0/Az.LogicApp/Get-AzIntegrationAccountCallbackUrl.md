---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190326"
---
# <span data-ttu-id="e5b25-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="e5b25-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="e5b25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5b25-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b25-103">Ottiene un URL di url personale dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e5b25-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="e5b25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5b25-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5b25-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5b25-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b25-106">Il **cmdlet Get-AzIntegrationAccountUrlUrl** ottiene l'URL url di url url dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5b25-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="e5b25-107">Questo cmdlet restituisce un oggetto **UrlUrl** che rappresenta l'URL url url dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e5b25-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="e5b25-108">Specificare il nome dell'account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5b25-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="e5b25-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="e5b25-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e5b25-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="e5b25-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e5b25-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="e5b25-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e5b25-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="e5b25-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e5b25-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5b25-113">EXAMPLES</span></span>

### <span data-ttu-id="e5b25-114">Esempio 1: Url url di url di un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="e5b25-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="e5b25-115">Questo comando ottiene l'URL url url dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e5b25-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="e5b25-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5b25-116">PARAMETERS</span></span>

### <span data-ttu-id="e5b25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b25-117">-DefaultProfile</span></span>
<span data-ttu-id="e5b25-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e5b25-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5b25-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e5b25-119">-Name</span></span>
<span data-ttu-id="e5b25-120">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e5b25-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b25-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="e5b25-121">-NotAfter</span></span>
<span data-ttu-id="e5b25-122">Specifica la data di scadenza per l'URL url.</span><span class="sxs-lookup"><span data-stu-id="e5b25-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b25-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b25-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5b25-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5b25-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b25-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b25-125">CommonParameters</span></span>
<span data-ttu-id="e5b25-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b25-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b25-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5b25-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b25-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5b25-128">INPUTS</span></span>

### <span data-ttu-id="e5b25-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e5b25-129">System.String</span></span>

## <span data-ttu-id="e5b25-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5b25-130">OUTPUTS</span></span>

### <span data-ttu-id="e5b25-131">Microsoft.Azure.Management.Logic.Models.Url</span><span class="sxs-lookup"><span data-stu-id="e5b25-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="e5b25-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5b25-132">NOTES</span></span>

## <span data-ttu-id="e5b25-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5b25-133">RELATED LINKS</span></span>

[<span data-ttu-id="e5b25-134">Get-AzLogicAppTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="e5b25-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


