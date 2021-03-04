---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: dbabc98a8221cc2b870368b2b9cdd55e81280863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994613"
---
# <span data-ttu-id="c85c9-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c85c9-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="c85c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c85c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c85c9-103">Ottiene il criterio di ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="c85c9-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="c85c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c85c9-104">SYNTAX</span></span>

### <span data-ttu-id="c85c9-105">GetTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c85c9-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c85c9-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="c85c9-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c85c9-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="c85c9-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c85c9-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="c85c9-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c85c9-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c85c9-109">DESCRIPTION</span></span>
<span data-ttu-id="c85c9-110">Il cmdlet **Get-AzApiManagementPolicy** ottiene il criterio di ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="c85c9-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="c85c9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c85c9-111">EXAMPLES</span></span>

### <span data-ttu-id="c85c9-112">Esempio 1: Ottenere i criteri a livello di tenant</span><span class="sxs-lookup"><span data-stu-id="c85c9-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="c85c9-113">Questo comando recupera i criteri a livello di tenant e lo salva in un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="c85c9-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="c85c9-114">Esempio 2: Ottenere i criteri di ambito del prodotto</span><span class="sxs-lookup"><span data-stu-id="c85c9-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="c85c9-115">Questo comando recupera i criteri di ambito del prodotto</span><span class="sxs-lookup"><span data-stu-id="c85c9-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="c85c9-116">Esempio 3: Ottenere il criterio di ambito API</span><span class="sxs-lookup"><span data-stu-id="c85c9-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="c85c9-117">Questo comando ottiene i criteri di ambito API.</span><span class="sxs-lookup"><span data-stu-id="c85c9-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="c85c9-118">Esempio 4: Ottenere il criterio di ambito delle operazioni</span><span class="sxs-lookup"><span data-stu-id="c85c9-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="c85c9-119">Questo comando recupera i criteri di ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c85c9-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="c85c9-120">Esempio 5: Ottenere il criterio di ambito tenant in formato RawXml</span><span class="sxs-lookup"><span data-stu-id="c85c9-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $apimContext -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="c85c9-121">Questo comando recupera i criteri dell'ambito tenant in formato di caratteri di escape non Xml.</span><span class="sxs-lookup"><span data-stu-id="c85c9-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="c85c9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c85c9-122">PARAMETERS</span></span>

### <span data-ttu-id="c85c9-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c85c9-123">-ApiId</span></span>
<span data-ttu-id="c85c9-124">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="c85c9-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="c85c9-125">Se si specifica questo parametro, il cmdlet restituisce il criterio di ambito API.</span><span class="sxs-lookup"><span data-stu-id="c85c9-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c85c9-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c85c9-126">-ApiRevision</span></span>
<span data-ttu-id="c85c9-127">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="c85c9-127">Identifier of API Revision.</span></span> <span data-ttu-id="c85c9-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c85c9-128">This parameter is optional.</span></span> <span data-ttu-id="c85c9-129">Se non viene specificato, il criterio verrà recuperato dalla revisione dell'API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="c85c9-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c85c9-130">-Context</span><span class="sxs-lookup"><span data-stu-id="c85c9-130">-Context</span></span>
<span data-ttu-id="c85c9-131">Specifica un'istanza di **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="c85c9-131">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c85c9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c85c9-132">-DefaultProfile</span></span>
<span data-ttu-id="c85c9-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c85c9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c85c9-134">-Force</span><span class="sxs-lookup"><span data-stu-id="c85c9-134">-Force</span></span>
<span data-ttu-id="c85c9-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="c85c9-135">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c85c9-136">-Format</span><span class="sxs-lookup"><span data-stu-id="c85c9-136">-Format</span></span>
<span data-ttu-id="c85c9-137">Specifica il formato dei criteri di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="c85c9-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="c85c9-138">Il valore predefinito per questo parametro è "xml".</span><span class="sxs-lookup"><span data-stu-id="c85c9-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="c85c9-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c85c9-139">-OperationId</span></span>
<span data-ttu-id="c85c9-140">Specifica l'identificatore dell'operazione API esistente.</span><span class="sxs-lookup"><span data-stu-id="c85c9-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="c85c9-141">Se si specifica questo parametro con *ApiId,* il cmdlet restituisce i criteri di ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c85c9-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c85c9-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c85c9-142">-ProductId</span></span>
<span data-ttu-id="c85c9-143">Specifica l'identificatore di un prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="c85c9-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="c85c9-144">Se si specifica questo parametro, il cmdlet restituisce i criteri dell'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c85c9-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c85c9-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="c85c9-145">-SaveAs</span></span>
<span data-ttu-id="c85c9-146">Specifica il percorso del file in cui salvare il risultato.</span><span class="sxs-lookup"><span data-stu-id="c85c9-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="c85c9-147">Se non si specifica questo parametro, il risultato viene pipelined come sting.</span><span class="sxs-lookup"><span data-stu-id="c85c9-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="c85c9-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c85c9-148">-Confirm</span></span>
<span data-ttu-id="c85c9-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c85c9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c85c9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c85c9-150">-WhatIf</span></span>
<span data-ttu-id="c85c9-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c85c9-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c85c9-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c85c9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c85c9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c85c9-153">CommonParameters</span></span>
<span data-ttu-id="c85c9-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c85c9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c85c9-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c85c9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c85c9-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="c85c9-156">INPUTS</span></span>

### <span data-ttu-id="c85c9-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c85c9-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c85c9-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c85c9-158">System.String</span></span>

### <span data-ttu-id="c85c9-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c85c9-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c85c9-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c85c9-160">OUTPUTS</span></span>

### <span data-ttu-id="c85c9-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c85c9-161">System.String</span></span>

## <span data-ttu-id="c85c9-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="c85c9-162">NOTES</span></span>

## <span data-ttu-id="c85c9-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c85c9-163">RELATED LINKS</span></span>

[<span data-ttu-id="c85c9-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c85c9-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="c85c9-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c85c9-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


