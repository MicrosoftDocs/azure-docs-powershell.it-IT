---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 6cbb37eb211c766959f2513abe3bbe1554bfdb23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510556"
---
# <span data-ttu-id="d8f7e-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d8f7e-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="d8f7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f7e-103">Ottiene un URL di callback dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8f7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8f7e-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f7e-106">Il cmdlet **Get-AzureRmIntegrationAccountCallbackUrl** ottiene un URL di callback dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="d8f7e-107">Questo cmdlet restituisce un oggetto **CallbackUrl** che rappresenta l'URL di callback dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="d8f7e-108">Specificare il nome dell'account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-108">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="d8f7e-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d8f7e-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d8f7e-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d8f7e-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d8f7e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8f7e-113">EXAMPLES</span></span>

### <span data-ttu-id="d8f7e-114">Esempio 1: ottenere un URL di callback dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="d8f7e-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="d8f7e-115">Questo comando ottiene un URL di callback dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="d8f7e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8f7e-116">PARAMETERS</span></span>

### <span data-ttu-id="d8f7e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8f7e-117">-Name</span></span>
<span data-ttu-id="d8f7e-118">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-118">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="d8f7e-119">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="d8f7e-119">-NotAfter</span></span>
<span data-ttu-id="d8f7e-120">Specifica la data di scadenza per l'URL di callback.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-120">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="d8f7e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f7e-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8f7e-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d8f7e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f7e-123">-DefaultProfile</span></span>
<span data-ttu-id="d8f7e-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f7e-125">CommonParameters</span></span>
<span data-ttu-id="d8f7e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f7e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f7e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f7e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8f7e-128">INPUTS</span></span>

## <span data-ttu-id="d8f7e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8f7e-129">OUTPUTS</span></span>

### <span data-ttu-id="d8f7e-130">Microsoft. Azure. Management. Logic. Models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d8f7e-130">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="d8f7e-131">Note</span><span class="sxs-lookup"><span data-stu-id="d8f7e-131">NOTES</span></span>

## <span data-ttu-id="d8f7e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8f7e-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8f7e-133">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d8f7e-133">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)

