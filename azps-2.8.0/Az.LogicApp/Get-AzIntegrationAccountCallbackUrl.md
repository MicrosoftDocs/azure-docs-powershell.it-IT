---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: e4046424a1388941af967782f9778177bcfbbb1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674044"
---
# <span data-ttu-id="ca551-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ca551-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="ca551-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca551-102">SYNOPSIS</span></span>
<span data-ttu-id="ca551-103">Ottiene un URL di callback dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ca551-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="ca551-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca551-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca551-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca551-105">DESCRIPTION</span></span>
<span data-ttu-id="ca551-106">Il cmdlet **Get-AzIntegrationAccountCallbackUrl** ottiene un URL di callback dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca551-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="ca551-107">Questo cmdlet restituisce un oggetto **CallbackUrl** che rappresenta l'URL di callback dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ca551-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="ca551-108">Specificare il nome dell'account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca551-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="ca551-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="ca551-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ca551-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="ca551-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ca551-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="ca551-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ca551-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="ca551-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ca551-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca551-113">EXAMPLES</span></span>

### <span data-ttu-id="ca551-114">Esempio 1: ottenere un URL di callback dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ca551-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="ca551-115">Questo comando ottiene un URL di callback dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ca551-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="ca551-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca551-116">PARAMETERS</span></span>

### <span data-ttu-id="ca551-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca551-117">-DefaultProfile</span></span>
<span data-ttu-id="ca551-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ca551-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca551-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca551-119">-Name</span></span>
<span data-ttu-id="ca551-120">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ca551-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ca551-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="ca551-121">-NotAfter</span></span>
<span data-ttu-id="ca551-122">Specifica la data di scadenza per l'URL di callback.</span><span class="sxs-lookup"><span data-stu-id="ca551-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="ca551-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca551-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca551-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca551-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ca551-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca551-125">CommonParameters</span></span>
<span data-ttu-id="ca551-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca551-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca551-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca551-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca551-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca551-128">INPUTS</span></span>

### <span data-ttu-id="ca551-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ca551-129">System.String</span></span>

## <span data-ttu-id="ca551-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca551-130">OUTPUTS</span></span>

### <span data-ttu-id="ca551-131">Microsoft. Azure. Management. Logic. Models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ca551-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="ca551-132">Note</span><span class="sxs-lookup"><span data-stu-id="ca551-132">NOTES</span></span>

## <span data-ttu-id="ca551-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca551-133">RELATED LINKS</span></span>

[<span data-ttu-id="ca551-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ca551-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)

